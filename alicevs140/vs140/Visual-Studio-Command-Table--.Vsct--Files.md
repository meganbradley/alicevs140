---
title: "Visual Studio Command Table (.Vsct) Files"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1313adb4-add4-4e74-90e2-f4be522f5259
caps.latest.revision: 24
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Visual Studio Command Table (.Vsct) Files
A command table configuration file is a text file that describes the set of commands that a VSPackage contains. The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] command table (VSCT) compiler compiles XML-based configuration files (.vsct files) into binary command table output (.cto) files. The resultant .cto files are the same as those that are created by using the command table (CTC) compiler to compile .ctc configuration files. However, XML-based .vsct files has some advantages, such as an XML editor and XML IntelliSense.  
  
 To learn more about the syntax and semantics of .vsct files, see [Designing XML Command Table (.vsct) Files](../Topic/Designing%20XML%20Command%20Table%20\(.Vsct\)%20Files.md)  
  
## In This Section  
 [Designing XML Command Table (.vsct) Files](../Topic/Designing%20XML%20Command%20Table%20\(.Vsct\)%20Files.md)  
 Describes how to design .vsct files.  
  
 [How To: Create a New .vsct File](../vs140/How-to--Create-a-.Vsct-File.md)  
 Compares the methods for creating a .vsct file. Describes the process for manually creating a new .vsct file.  
  
## Related Sections  
 [Command Table Compiler  XML Schema Reference](../vs140/VSCT-XML-Schema-Reference.md)  
 Provides details about each section of the command table XML configuration file.  
  
 [Command Table Configuration (.Ctc) Files](assetId:///3413dda1-f372-4669-bcf0-c64d3463842c)  
 Presents an overview of the deprecated .ctc file format.  
  
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)  
 Describes the command table format specification.  
  
 [Resources in Managed VSPackages](../Topic/Resources%20in%20VSPackages.md)  
 Describes how to use managed and unmanaged resources in managed VSPackages.  
  
 [Menus and Toolbars](../Topic/Commands,%20Menus,%20and%20Toolbars.md)  
 Explains how to create a UI that includes menus, toolbars, and command combo boxes.