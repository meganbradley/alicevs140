---
title: "How to: Copy Files with a Specific Pattern to a Directory in Visual Basic"
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
ms.assetid: f205d2ad-bbe5-4d55-8a40-acda21aa82dd
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Copy Files with a Specific Pattern to a Directory in Visual Basic
The <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles?qualifyHint=False> method returns a read-only collection of strings representing the path names for the files. You can use the `wildCards` parameter to specify a specific pattern.  
  
 An empty collection is returned if no matching files are found.  
  
 You can use the <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile?qualifyHint=False> method to copy the files to a directory.  
  
### To copy files with a specific pattern to a directory  
  
1.  Use the `GetFiles` method to return the list of files. This example returns all .rtf files in the specified directory.  
  
     [!CODE [VbFileIOMisc#36](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOMisc#36)]  
  
2.  Use the `CopyFile` method to copy the files. This example copies the files to the directory named `testdirectory`.  
  
     [!CODE [VbVbcnMyFileSystem#88](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#88)]  
  
3.  Close the `For` statement with a `Next` statement.  
  
     [!CODE [VbVbcnMyFileSystem#89](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#89)]  
  
## Example  
 The following example, which presents the above snippets in complete form, copies all .rtf files in the specified directory to the directory named `testdirectory`.  
  
 [!CODE [VbFileIOMisc#37](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOMisc#37)]  
  
## .NET Framework Security  
 The following conditions may cause an exception:  
  
-   The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException?qualifyHint=False>).  
  
-   The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException?qualifyHint=False>).  
  
-   The directory does not exist (<xref:System.IO.DirectoryNotFoundException?qualifyHint=False>).  
  
-   The directory points to an existing file (<xref:System.IO.IOException?qualifyHint=False>).  
  
-   The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException?qualifyHint=False>).  
  
-   A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException?qualifyHint=False>).  
  
-   The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException?qualifyHint=False>). The user lacks necessary permissions (<xref:System.UnauthorizedAccessException?qualifyHint=False>).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles?qualifyHint=False>   
 [How to: Find Subdirectories with a Specific Pattern](../Topic/How%20to:%20Find%20Subdirectories%20with%20a%20Specific%20Pattern%20in%20Visual%20Basic.md)   
 [Troubleshooting: Reading from and Writing to Text Files](../vs140/Troubleshooting--Reading-from-and-Writing-to-Text-Files--Visual-Basic-.md)   
 [How to: Get the Collection of Files in a Directory in Visual Basic](../Topic/How%20to:%20Get%20the%20Collection%20of%20Files%20in%20a%20Directory%20in%20Visual%20Basic.md)