
# Common.CET
A collection of common CET tasks and codes. 

I hope you enjoy and, *feel free to send Pull Requests with suggestions*!

# License

Every single snippet of code here is shared under CETSC.

### Configura CET Source Copyright Notice (CETSC)

> Configura CET Source Copyright Notice (CETSC)
> 
>    This file contains Configura CM source code and is part of the   
> Configura CET Development Platform (CETDEV). Configura CM    is a
> programming language created by Configura Sverige AB.    Configura,
> Configura CET and Configura CM are trademarks of    Configura Sverige
> AB. Configura Sverige AB owns Configura CET,    Configura CM, and
> CETDEV.
> 
>    Copyright (C) 2004 Configura Sverige AB, All rights reserved.
> 
>    You can modify this source file under the terms of the Configura
> CET    Source Licence Agreement (CETSL) as published by Configura
> Sverige AB.
> 
>    Configura Sverige AB has exclusive rights to all changes,
> modifications,    and corrections of this source file. Configura
> Sverige AB has exclusive    rights to any new source file containing
> material from this source file.    A new source file based on this
> source file or containing material from    this source file has to
> include this Configura CET Source Copyright Notice    in its full
> content. All changes, modifications, and corrections mentioned   
> above shall be reported to Configura Sverige AB within One Month from 
> the date that the modification occurred.
> 
>    Configura CM is distributed in the hope that it will be useful, but
> WITHOUT ANY WARRANTY; without even the implied warranty of   
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.    See the CETSL
> for more details.
> 
>    You should have received a copy of the CETSL along with the CETDEV.
> If not, write to Configura Sverige AB, Box 306, SE-581 02 Linköping,
> Sweden.    Tel +46 13377800, Fax +46 13377855,    Email:
> info@configura.com, www.configura.com
> 
>    END OF CETSC

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
