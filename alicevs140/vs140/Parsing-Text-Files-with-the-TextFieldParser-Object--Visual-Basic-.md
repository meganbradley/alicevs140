---
title: "Parsing Text Files with the TextFieldParser Object (Visual Basic)"
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
ms.assetid: fc31d6e6-af0c-403f-8a00-d556b2c57567
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parsing Text Files with the TextFieldParser Object (Visual Basic)
The `TextFieldParser` object allows you to parse and process very large file that are structured as delimited-width columns of text, such as log files or legacy database information. Parsing a text file with `TextFieldParser` is similar to iterating over a text file, while the parse method to extract fields of text is similar to string manipulation methods used to tokenize delimited strings.  
  
## Parsing Different Types of Text Files  
 Text files may have fields of various width, delimited by a character such as a comma or a tab space. Define `TextFieldType` and the delimiter, as in the following example, which uses the `SetDelimiters` method to define a tab-delimited text file:  
  
 [!CODE [VbVbalrTextFieldParser#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTextFieldParser#21)]  
  
 Other text files may have field widths that are fixed. In such cases, you need to define the `TextFieldType` as `FixedWidth` and define the widths of each field, as in the following example. This example uses the `SetFieldWidths` method to define the columns of text: the first column is 5 characters wide, the second is 10, the third is 11, and the fourth is of variable width.  
  
 [!CODE [VbVbalrTextFieldParser#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTextFieldParser#22)]  
  
 Once the format is defined, you can loop through the file, using the `ReadFields` method to process each line in turn.  
  
 If a field does not match the specified format, a <xref:Microsoft.VisualBasic.FileIO.MalformedLineException?qualifyHint=False> exception is thrown. When such exceptions are thrown, the `ErrorLine` and `ErrorLineNumber` properties hold the text causing the exception and the line number of that text.  
  
## Parsing Files with Multiple Formats  
 The `PeekChars` method of the `TextFieldParser` object can be used to check each field before reading it, allowing you to define multiple formats for the fields and react accordingly. For more information, see [How to: Read From Text Files with Multiple Formats in Visual Basic](../Topic/How%20to:%20Read%20From%20Text%20Files%20with%20Multiple%20Formats%20in%20Visual%20Basic.md).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFieldParser?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.PeekChars?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ReadFields?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLineNumber?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.FieldWidths?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.HasFieldsEnclosedInQuotes?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.LineNumber?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TextFieldType?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TrimWhiteSpace?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetFieldWidths?qualifyHint=False>   
 [Troubleshooting Exceptions: Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException](../Topic/Troubleshooting%20Exceptions:%20Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException.md)