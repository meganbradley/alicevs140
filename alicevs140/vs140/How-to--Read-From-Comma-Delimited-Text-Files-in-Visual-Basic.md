---
title: "How to: Read From Comma-Delimited Text Files in Visual Basic"
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
ms.assetid: a8413fe4-0dba-49c8-8692-44fb67a9ec4f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Read From Comma-Delimited Text Files in Visual Basic
The `TextFieldParser` object provides a way to easily and efficiently parse structured text files, such as logs. The `TextFieldType` property defines whether it is a delimited file or one with fixed-width fields of text.  
  
### To parse a comma delimited text file  
  
1.  Create a new `TextFieldParser`. The following code creates the `TextFieldParser` named `MyReader` and opens the file `test.txt`.  
  
     [!CODE [VbFileIORead#15](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#15)]  
  
2.  Define the `TextField` type and delimiter. The following code defines the `TextFieldType` property as `Delimited` and the delimiter as ",".  
  
     [!CODE [VbFileIORead#16](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#16)]  
  
3.  Loop through the fields in the file. If any lines are corrupt, report an error and continue parsing. The following code loops through the file, displaying each field in turn and reporting any fields that are formatted incorrectly.  
  
     [!CODE [VbFileIORead#17](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#17)]  
  
4.  Close the `While` and `Using` blocks with `End While` and `End Using`.  
  
     [!CODE [VbFileIORead#18](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#18)]  
  
## Example  
 This example reads from the file `test.txt`.  
  
 [!CODE [VbFileIORead#19](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#19)]  
  
## Robust Programming  
 The following conditions may cause an exception:  
  
-   A row cannot be parsed using the specified format (<xref:Microsoft.VisualBasic.FileIO.MalformedLineException?qualifyHint=False>). The exception message specifies the line causing the exception, while the <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine?qualifyHint=False> property is assigned the text contained in the line.  
  
-   The specified file does not exist (<xref:System.IO.FileNotFoundException?qualifyHint=False>).  
  
-   A partial-trust situation in which the user does not have sufficient permissions to access the file. (<xref:System.Security.SecurityException?qualifyHint=False>).  
  
-   The path is too long (<xref:System.IO.PathTooLongException?qualifyHint=False>).  
  
-   The user does not have sufficient permissions to access the file (<xref:System.UnauthorizedAccessException?qualifyHint=False>).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?qualifyHint=True>   
 [How to: Read From a Fixed-width Text File in Visual Basic](../Topic/How%20to:%20Read%20From%20Fixed-width%20Text%20Files%20in%20Visual%20Basic.md)   
 [How to: Read From a Text File with Multiple Formats in Visual Basic](../Topic/How%20to:%20Read%20From%20Text%20Files%20with%20Multiple%20Formats%20in%20Visual%20Basic.md)   
 [Parsing Text Files with the TextFieldParser Object](../vs140/Parsing-Text-Files-with-the-TextFieldParser-Object--Visual-Basic-.md)   
 [Walkthrough: Manipulating Files and Directories in Visual Basic](../vs140/Walkthrough--Manipulating-Files-and-Directories-in-Visual-Basic.md)   
 [Troubleshooting: Reading from and Writing to Text Files](../vs140/Troubleshooting--Reading-from-and-Writing-to-Text-Files--Visual-Basic-.md)   
 [Troubleshooting Exceptions: Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException](../Topic/Troubleshooting%20Exceptions:%20Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException.md)