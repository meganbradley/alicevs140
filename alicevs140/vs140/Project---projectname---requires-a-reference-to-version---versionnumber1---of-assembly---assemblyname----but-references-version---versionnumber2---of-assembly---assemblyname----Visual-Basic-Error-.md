---
title: "Project &#39;&lt;projectname&gt;&#39; requires a reference to version &#39;&lt;versionnumber1&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39;, but references version &#39;&lt;versionnumber2&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39; (Visual Basic Error)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe50736b-444f-4e40-8f80-9760ff13a153
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project &#39;&lt;projectname&gt;&#39; requires a reference to version &#39;&lt;versionnumber1&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39;, but references version &#39;&lt;versionnumber2&gt;&#39; of assembly &#39;&lt;assemblyname&gt;&#39; (Visual Basic Error)
A project makes an indirect reference to an assembly that is defined elsewhere, but the project also has a direct reference to a later version of that assembly.  
  
 If the compiler allowed your code to use the indirect reference, you might not be able to access types and programming elements that are defined in the later version but not in the earlier version.  
  
 **Error ID:** BC32209  
  
### To correct this error  
  
-   Remove the indirect reference to the earlier version of the assembly, and use the direct reference to the later version.  
  
## See Also  
 [Assemblies Overview](assetId:///2cfebe19-7436-49f1-bd99-3c4019f0b676)   
 [NIB: Referencing Namespaces and Components](assetId:///568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Project References](../Topic/Managing%20references%20in%20a%20project.md)   
 [NIB: Managing References](assetId:///910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)