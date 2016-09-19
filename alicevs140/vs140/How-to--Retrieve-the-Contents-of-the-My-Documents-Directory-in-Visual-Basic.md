---
title: "How to: Retrieve the Contents of the My Documents Directory in Visual Basic"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 26560d01-7dda-4457-8e95-21db23d71aea
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Retrieve the Contents of the My Documents Directory in Visual Basic
The <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories?qualifyHint=False> object can be used to read from many of the **All Users** directories, such as **My Documents** or **Desktop**.  
  
### To read from the My Documents folder  
  
-   Use the `ReadAllText` method to read the text from each file in a specific directory. The following code specifies a directory and file and then uses `ReadAllText` to read them into the string named `patients`.  
  
     [!CODE [VbVbcnMyFileSystem#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#15)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText?qualifyHint=False>