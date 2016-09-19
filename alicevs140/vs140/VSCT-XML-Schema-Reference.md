---
title: "VSCT XML Schema Reference"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49e7efae-e713-4762-a824-96fdaf92cdc9
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# VSCT XML Schema Reference
Provides a table of Command Table Compiler schema elements, with allowed child elements and attributes for each.  
  
 An XML-based command table configuration (.vsct) file defines the command elements that a VSPackage provides to the integrated development environment (IDE). These elements include menu items, menus, toolbars, and combo boxes.  
  
> [!NOTE]
>  The VSCT compiler can run a preprocessor on the .vsct file. Because this is typically the C++ preprocessor, you can define includes and macros that have the same syntax that is used in C++ files. Examples of this are provided in the .vsct file that the **New Project** wizard creates for a VSPackage project.  
  
## Optional Elements  
 Some VSCT elements are optional. If a `Parent` argument is not specified, Group_Undefined:0 will be implied. If an `Icon` argument is not specified, guidOfficeIcon:msotcidNoIcon will be implied. When a shortcut key is defined, the emulation, which is typically unused, is optional.  
  
 Bitmap items may be embedded at compile time by specifying the location of the bitmap strip in the `href` argument. The bitmap strip is copied during the merge rather than extracted from the resources of the DLL. When an `href` argument is provided, the `usedList` argument becomes optional, and all slots in the bitmap strip are considered used.  
  
 All GUID and ID values must be defined by using symbolic names. These names may be defined in header files or in VSCT <Symbols\> sections. The symbolic names must be local, included through <Include\> elements, or referenced by <Extern\> elements. A symbolic name is imported from a header file specified in an <Extern\> element if it follows the simple pattern of #define SYMBOL   VALUE. The value may be another symbol as long as that symbol was previously defined. GUID definitions must follow either the OLE or C++ format. ID values may be either decimal digits or hexadecimal digits that are preceded by 0x, as shown in the following lines:  
  
-   {6D484634-E53D-4a2c-ADCB-55145C9362C8}  
  
-   { 0x6d484634, 0xe53d, 0x4a2c, { 0xad, 0xcb, 0x55, 0x14, 0x5c, 0x93, 0x62, 0xc8 } }  
  
 XML comments may be used, but round-trip graphical user interface (GUI) tools might discard them. The contents of <Annotation\> elements are guaranteed to be maintained regardless of format.  
  
## Schema Hierarchy  
 A .vsct file has the following major elements.  
  
 [CommandTable Element](../vs140/CommandTable-Element.md)  
  
 [Extern Element](../vs140/Extern-Element.md)  
  
 [Include Element](../vs140/Include-Element.md)  
  
 [Define Element](../vs140/Define-Element.md)  
  
 [Commands Element](../vs140/Commands-Element.md)  
  
 [CommandPlacements Element](../vs140/CommandPlacements-Element.md)  
  
 [VisibilityConstraints Element](../vs140/VisibilityConstraints-Element.md)  
  
 [KeyBindings Element](../vs140/KeyBindings-Element.md)  
  
 [UsedCommands Element](../vs140/UsedCommands-Element.md)  
  
 [Parent Element](../vs140/Parent-Element.md)  
  
 [Icon Element](../vs140/Icon-Element.md)  
  
 [Strings Element](../vs140/Strings-Element.md)  
  
 [Command Flag Element](../vs140/Command-Flag-Element.md)  
  
 [Symbols Element](../vs140/Symbols-Element.md)  
  
 [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md)  
  
## See Also  
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)   
 [Command Routing in the Visual Studio SDK](../vs140/Command-Routing-in-VSPackages.md)