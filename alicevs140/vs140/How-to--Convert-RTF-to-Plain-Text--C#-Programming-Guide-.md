---
title: "How to: Convert RTF to Plain Text (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b386a87-899d-4d98-bc82-a980526ddaac
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert RTF to Plain Text (C# Programming Guide)
Rich Text Format (RTF) is a document format developed by Microsoft in the late 1980s to enable the exchange of documents across operating systems. Both Microsoft Word and WordPad can read and write RTF documents. In the .NET Framework, you can use the <xref:System.Windows.Forms.RichTextBox?qualifyHint=False> control to create a word processor that supports RTF and enables a user to apply formatting to text in a WYSIWIG manner.  
  
 You can also use the <xref:System.Windows.Forms.RichTextBox?qualifyHint=False> control to programmatically remove the RTF formatting codes from a document and convert it to plain text. You do not need to embed the control in a Windows Form to perform this kind of operation.  
  
### To use the RichTextBox control in a project  
  
1.  Add a reference to System.Windows.Forms.dll.  
  
2.  Add a using directive for the `System.Windows.Forms` namespace (optional).  
  
## Example  
 The following example converts a sample RTF file to plain text. The file contains RTF formatting (such as font information), four Unicode characters, and four extended ASCII characters. The example code opens the file, passes its content to a <xref:System.Windows.Forms.RichTextBox?qualifyHint=False> as RTF, retrieves the content as text, displays the text in a <xref:System.Windows.Forms.MessageBox?qualifyHint=False>, and outputs the text to a file in UTF-8 format.  
  
 The `MessageBox` and the output file contain the following text:  
  
```  
The Greek word for "psyche" is spelled ψυχή. The Greek letters are encoded in Unicode.  
These characters are from the extended ASCII character set (Windows code page 1252):  âäӑå  
  
```  
  
 [!CODE [csProgGuideStrings#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStrings#33)]  
  
 RTF characters are encoded in eight bits. However, users can specify Unicode characters in addition to extended ASCII characters from specified code pages. Because the <xref:System.Windows.Forms.RichTextBox.Text?qualifyHint=True> property is of type [string](../Topic/string%20\(C%23%20Reference\).md), the characters are encoded as Unicode UTF-16. Any extended ASCII characters and Unicode characters from the source RTF document are correctly encoded in the text output.  
  
 If you use the <xref:System.IO.File.WriteAllText?qualifyHint=True> method to write the text to disk, the text will be encoded as UTF-8 (without a Byte Order Mark).  
  
## See Also  
 <xref:System.Windows.Forms.RichTextBox?qualifyHint=True>   
 [Strings Overview (C# Programming Guide)](../Topic/Strings%20\(C%23%20Programming%20Guide\).md)