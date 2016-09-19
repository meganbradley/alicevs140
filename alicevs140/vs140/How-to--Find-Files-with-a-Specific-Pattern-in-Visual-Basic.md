---
title: "How to: Find Files with a Specific Pattern in Visual Basic"
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
ms.assetid: 25e3b71d-b844-4293-9e4e-f06c5836b5cc
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Find Files with a Specific Pattern in Visual Basic
The <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles?qualifyHint=False> method returns a read-only collection of strings representing the path names for the files. You can use the `wildCards` parameter to specify a specific pattern. If you would like to include subdirectories in the search, set the `searchType` parameter to `SearchOption.SearchAllSubDirectories`.  
  
 An empty collection is returned if no files matching the specified pattern are found.  
  
> [!NOTE]
>  For information about returning a file list by using the `DirectoryInfo` class of the `System.IO` namespace, see <xref:System.IO.DirectoryInfo.GetFiles?qualifyHint=False>.  
  
### To find files with a specified pattern  
  
-   Use the `GetFiles` method, supplying the name and path of the directory you want to search and specifying the pattern. The following example returns all files with the extension `.dll` in the directory and adds them to `ListBox1`.  
  
     [!CODE [VbFileIOMisc#4](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOMisc#4)]  
  
## .NET Framework Security  
 The following conditions may cause an exception:  
  
-   The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException?qualifyHint=False>).  
  
-   The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException?qualifyHint=False>).  
  
-   `directory` does not exist (<xref:System.IO.DirectoryNotFoundException?qualifyHint=False>).  
  
-   `directory` points to an existing file (<xref:System.IO.IOException?qualifyHint=False>).  
  
-   The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException?qualifyHint=False>).  
  
-   A file or folder name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException?qualifyHint=False>).  
  
-   The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException?qualifyHint=False>).  
  
-   The user lacks necessary permissions (<xref:System.UnauthorizedAccessException?qualifyHint=False>).  
  
## See Also  
 <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles?qualifyHint=False>   
 [How to: Find Subdirectories with a Specific Pattern](../Topic/How%20to:%20Find%20Subdirectories%20with%20a%20Specific%20Pattern%20in%20Visual%20Basic.md)   
 [Troubleshooting: Reading from and Writing to Text Files](../vs140/Troubleshooting--Reading-from-and-Writing-to-Text-Files--Visual-Basic-.md)   
 [How to: Get the Collection of Files in a Directory in Visual Basic](../Topic/How%20to:%20Get%20the%20Collection%20of%20Files%20in%20a%20Directory%20in%20Visual%20Basic.md)