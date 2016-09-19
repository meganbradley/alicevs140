---
title: "Assembly &#39;&lt;filepath1&gt;&#39; references assembly &#39;&lt;assemblyidentity&gt;&#39;, which is ambiguous between &#39;&lt;filepath2&gt;&#39; and &#39;&lt;filepath3&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c36feb10-dded-4073-9553-af278ae5560b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Assembly &#39;&lt;filepath1&gt;&#39; references assembly &#39;&lt;assemblyidentity&gt;&#39;, which is ambiguous between &#39;&lt;filepath2&gt;&#39; and &#39;&lt;filepath3&gt;&#39;
Assembly '<filepath1\>' references assembly '<assemblyidentity\>', which is ambiguous between '<filepath2\>' and '<filepath3\>'. '<filepath2\>' will be used.  
  
 An assembly accesses a type in another assembly to which it has more than one file reference.  
  
 The compiler cannot guarantee that the files at the different locations hold the same version of the same assembly. Therefore, the file references are ambiguous and the compiler must select one.  
  
 The *assembly identity* includes the assembly's name, version, public key if any, and culture. This information uniquely identifies the assembly.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42205  
  
### To correct this error  
  
1.  Determine which file represents the best choice for the assembly. You might use criteria such as the most recent version, accessibility of the file, and likelihood of being updated when appropriate.  
  
2.  Change all file references to this assembly so they use the identical file path to your chosen file.  
  
## See Also  
 [NOT IN BUILD: Assemblies](assetId:///6c5c7b30-fa78-4f40-b908-120d0743b0e6)   
 [Assemblies Overview](assetId:///2cfebe19-7436-49f1-bd99-3c4019f0b676)   
 [Assembly Benefits](assetId:///77e1831e-9b6d-4a86-91a6-51e1a64271d9)   
 [Project References](../Topic/Managing%20references%20in%20a%20project.md)   
 [NIB: Managing References](assetId:///910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)