---
title: "How to: Create a Directory in Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0351a2ca-24d8-43b5-bb39-9b99e6401cff
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Directory in Visual Basic
Use the `CreateDirectory` method of the `My.Computer.FileSystem` object to create directories.  
  
 If the directory already exists, no exception is thrown.  
  
### To create a directory  
  
-   Use the `CreateDirectory` method by specifying the full path of the location where the directory should be created. This example creates the directory `NewDirectory` in `C:\Documents and Settings\All Users\Documents`.  
  
     [!CODE [VbVbcnMyFileSystem#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#2)]  
  
## Robust Programming  
 The following conditions may cause an exception:  
  
-   The directory name is malformed. For example, it contains illegal characters or is only white space (<xref:System.ArgumentException?qualifyHint=False>).  
  
-   The parent directory of the directory to be created is read-only (<xref:System.IO.IOException?qualifyHint=False>).  
  
-   The directory name is `Nothing` (<xref:System.ArgumentNullException?qualifyHint=False>).  
  
-   The directory name is too long (<xref:System.IO.PathTooLongException?qualifyHint=False>).  
  
-   The directory name is a colon ":" (<xref:System.NotSupportedException?qualifyHint=False>).  
  
-   The user does not have permission to create the directory (<xref:System.UnauthorizedAccessException?qualifyHint=False>).  
  
-   The user lacks permissions in a partial-trust situation (<xref:System.Security.SecurityException?qualifyHint=False>).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.CreateDirectory?qualifyHint=False>   
 [Creating, Deleting, and Moving Files and Directories in Visual Basic](../Topic/Creating,%20Deleting,%20and%20Moving%20Files%20and%20Directories%20in%20Visual%20Basic.md)