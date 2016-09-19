---
title: "Project &#39;&lt;projectname&gt;&#39; requires a reference to version &#39;&lt;versionnumber1&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39;, but references version &#39;&lt;versionnumber2&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39; (Visual Basic Warning)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 26a3fa34-ec5d-4817-a947-3959446a924a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project &#39;&lt;projectname&gt;&#39; requires a reference to version &#39;&lt;versionnumber1&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39;, but references version &#39;&lt;versionnumber2&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39; (Visual Basic Warning)
Project '<projectname\>' requires a reference to version '<versionnumber1\>' of assembly '<assemblyname\>', but references version '<versionnumber2\>' of assembly '<assemblyname\>'. Reference to version '<versionnumber1\>' emitted.  
  
 A project makes an indirect reference to an assembly that is defined elsewhere, but the project also has a direct reference to an earlier version of that assembly.  
  
 To accommodate access to types and programming elements defined in the later version but not in the earlier version, the compiler uses the indirect reference to the later version when resolving accesses.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42203  
  
### To correct this error  
  
-   Remove the direct reference to the earlier version of the assembly, or change it to refer to the later version.  
  
## See Also  
 [Assemblies Overview](assetId:///2cfebe19-7436-49f1-bd99-3c4019f0b676)   
 [NIB: Referencing Namespaces and Components](assetId:///568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Project References](../Topic/Managing%20references%20in%20a%20project.md)   
 [NIB: Managing References](assetId:///910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)