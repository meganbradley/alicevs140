---
title: "How to: Search Strings Using Regular Expressions (C# Programming Guide)"
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
ms.assetid: dcab2150-a4a2-4fe4-87e3-83b83b58d84a
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Search Strings Using Regular Expressions (C# Programming Guide)
The <xref:System.Text.RegularExpressions.Regex?qualifyHint=True> class can be used to search strings. These searches can range in complexity from very simple to making full use of regular expressions. The following are two examples of string searching by using the <xref:System.Text.RegularExpressions.Regex?qualifyHint=False> class. For more information, see [.NET Framework Regular Expressions](assetId:///521b3f6d-f869-42e1-93e5-158c54a6895d).  
  
## Example  
 The following code is a console application that performs a simple case-insensitive search of the strings in an array. The static method <xref:System.Text.RegularExpressions.Regex.IsMatch?qualifyHint=True> performs the search given the string to search and a string that contains the search pattern. In this case, a third argument is used to indicate that case should be ignored. For more information, see <xref:System.Text.RegularExpressions.RegexOptions?qualifyHint=True>.  
  
 [!CODE [csProgGuideStrings#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStrings#17)]  
  
## Example  
 The following code is a console application that uses regular expressions to validate the format of each string in an array. The validation requires that each string take the form of a telephone number in which three groups of digits are separated by dashes, the first two groups contain three digits, and the third group contains four digits. This is done by using the regular expression `^\\d{3}-\\d{3}-\\d{4}$`. For more information, see [Regular Expression Language Elements](assetId:///930653a6-95d2-4697-9d5a-52d11bb6fd4c).  
  
 [!CODE [csProgGuideStrings#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStrings#18)]  
  
## See Also  
 <xref:System.Text.RegularExpressions.Regex?qualifyHint=True>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Strings Overview (C# Programmer's Reference)](../Topic/Strings%20\(C%23%20Programming%20Guide\).md)   
 [.NET Framework Regular Expressions](assetId:///521b3f6d-f869-42e1-93e5-158c54a6895d)   
 [Regular Expression Language Elements](assetId:///930653a6-95d2-4697-9d5a-52d11bb6fd4c)