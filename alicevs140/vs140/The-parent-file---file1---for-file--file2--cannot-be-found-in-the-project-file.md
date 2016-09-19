---
title: "The parent file, &#39;file1&#39;, for file &#39;file2&#39; cannot be found in the project file"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1902c0b5-d09d-49b9-8f71-e325f7b9cfd7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The parent file, &#39;file1&#39;, for file &#39;file2&#39; cannot be found in the project file
The project system cannot find a node corresponding to a file.  
  
 Dependent files are persisted in the project file by adding a `DependentUpon` attribute to the `<File>` node. For example:  
  
```  
<File  
    RelPath = "Form1.resx"  
    SubType = "Code"  
    BuildAction = "EmbeddedResource"  
    DependentUpon="Form1.vb"  
/>  
```  
  
 This will make Form1.resx appear below Form1.vb in the project hierarchy.  
  
 This error is most likely caused by editing the project file by hand.  
  
### To correct this error  
  
-   Edit and update the project file.  
  
     The affected files will be added to the project, however, the dependency will not be preserved.  
  
## See Also  
 [NIB: Project Properties (Visual Studio)](assetId:///eb4c97ed-f667-4850-98d0-6e2a4d21bbca)