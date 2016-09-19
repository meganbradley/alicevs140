---
title: "How to: Write Text to Files in Visual Basic"
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
ms.assetid: 304956eb-530d-4df7-b48f-9b4d1f2581a0
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Write Text to Files in Visual Basic
The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText?qualifyHint=False> method can be used to write text to files. If the specified file does not exist, it is created.  
  
## Procedure  
  
#### To write text to a file  
  
-   Use the `WriteAllText` method to write text to a file, specifying the file and text to be written. This example writes the line `"This is new text."` to the file named `test.txt`, appending the text to any existing text in the file.  
  
     [!CODE [VbFileIOWrite#3](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#3)]  
  
#### To write a series of strings to a file  
  
-   Loop through the string collection. Use the `WriteAllText` method to write text to a file, specifying the target file and string to be added and setting `append` to `True`.  
  
     This example writes the names of the files in the `Documents and Settings` directory to `FileList.txt`, inserting a carriage return between each for better readability.  
  
     [!CODE [VbFileIOWrite#4](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#4)]  
  
## Robust Programming  
 The following conditions may cause an exception:  
  
-   The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException?qualifyHint=False>).  
  
-   The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException?qualifyHint=False>).  
  
-   `File` points to a path that does not exist (<xref:System.IO.FileNotFoundException?qualifyHint=False> or <xref:System.IO.DirectoryNotFoundException?qualifyHint=False>).  
  
-   The file is in use by another process, or an I/O error occurs (<xref:System.IO.IOException?qualifyHint=False>).  
  
-   The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException?qualifyHint=False>).  
  
-   A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException?qualifyHint=False>).  
  
-   The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException?qualifyHint=False>).  
  
-   The disk is full, and the call to `WriteAllText` fails (<xref:System.IO.IOException?qualifyHint=False>).  
  
 If you are running in a partial-trust context, the code might throw an exception due to insufficient privileges. For more information, see [Code Access Security Basics](assetId:///4eaa6535-d9fe-41a1-91d8-b437cfc16921).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText?qualifyHint=False>   
 [How to: Read From Text Files in Visual Basic](../Topic/How%20to:%20Read%20From%20Text%20Files%20in%20Visual%20Basic.md)