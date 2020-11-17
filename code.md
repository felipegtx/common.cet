
# Index

 1.  Embedded files
 2. `.rs` Files
    - Loading `.rs` Files 
    - Load order


# Embedded Files
In order to pack files (be it a `PNG`, `CM3D`, `.RS`, etc) inside your extension all you need to do is to return it inside the `package ExtensionInfo getExtensionInfo() : referred {` method.  

Here's and example:
```java
/**
* Actual extension info, dont change function name
*/
package ExtensionInfo getExtensionInfo() : referred {
    ExtensionInfo info = loadExtensionInfoFromXml(#:package);
    Url[] files();
    files << cmNative("custom/myextension/resources/*.rs");
    files << cmNative("custom/myextension/images/*.png");
    files << cmNative("custom/myextension/randomStuff/*.*");
    info.filesToInclude = files;
    return info;
}
```

# `.rs` Files

Resource files are super useful but it's not always fun to go through the process of making sure they are properly set up for you extension/package.

## Loading `.rs` files

Your files need to be properly registered in the extension. The right place to do so is inside the method `public  void  initialize(ExtensionEnv env)` on your `ToolboxCatalogExtension` class (e.g.: `UltraLazyExtension`).

The way to do so is by calling `safeLoadRs` along with `cmFindUrl` .

Here's an example if we wanted to embed `cm/core/core.rs` into our extension:  `safeLoadRs(cmFindUrl("cm/core/core.rs"));`

## Load order
By calling the method `putNextRsPkg` you get to build a priority lookup graph in which CET will look in order to fetch the correct description for your `$label`. The first parameter is the `parent` package that will be searched for and, the second parameter is the fallback option (in case a given resource is not found on the `parent`).

Calls to the `putNextRsPkg` are also usually set up inside the Extension's `public  void  initialize(ExtensionEnv env)`    method.

Here's an example that first searches for resource inside the package `custom.mypackage` and, if nothing is found, falls back to `cm.abstract.office`: `putNextRsPkg("custom.mypackage", "cm.abstract.office")`;
