---
title: "Troubleshooting: Reading from and Writing to Text Files (Visual Basic)"
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
ms.assetid: a8e9b44d-facb-4718-8c0f-466537171182
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting: Reading from and Writing to Text Files (Visual Basic)
This topic discusses common problems encountered when working with text files and suggests an approach to each.  
  
## Common Problems  
 The most common issues encountered when working with text files include security exceptions, file encodings, or invalid paths.  
  
### Security Exceptions  
 A <xref:System.Security.SecurityException?qualifyHint=False> is thrown when a security error occurs. This is often a result of the user lacking necessary permissions, which may be solved by adding permissions or working with files in isolated storage. For more information, see [Troubleshooting Exceptions: System.Security.SecurityException](../vs140/Troubleshooting-Exceptions--System.Security.SecurityException.md).  
  
### File Encodings  
 File encodings, also known as character encodings, specify how to represent characters when text processing. Unexpected characters in a text file may result from incorrect encoding. For most files, one encoding may be preferable over another in terms of which language characters it can or cannot handle, although Unicode is usually preferred. For more information, see [File Encodings](../vs140/File-Encodings--Visual-Basic-.md) and <xref:System.Text.Encoding?qualifyHint=False>.  
  
### Incorrect Paths  
 When parsing file paths, particularly relative paths, it is easy to supply the wrong data. Many problems can be corrected by making sure you are supplying the correct path. For more information, see [How to: Parse File Paths in Visual Basic](../Topic/How%20to:%20Parse%20File%20Paths%20in%20Visual%20Basic.md).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem?qualifyHint=False>   
 [Reading from Files in Visual Basic](../Topic/Reading%20from%20Files%20in%20Visual%20Basic.md)   
 [Writing to Files in Visual Basic](../Topic/Writing%20to%20Files%20in%20Visual%20Basic.md)   
 [Parsing Text Files with the TextFieldParser Object](../vs140/Parsing-Text-Files-with-the-TextFieldParser-Object--Visual-Basic-.md)