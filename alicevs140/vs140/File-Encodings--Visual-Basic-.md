---
title: "File Encodings (Visual Basic)"
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
ms.assetid: ea2c5f5f-bbb1-4150-9928-b9951fa6bc57
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File Encodings (Visual Basic)
File encodings, also known as character encodings, specify how to represent characters when text processing. One encoding may be preferable over another in terms of which language characters it can or cannot handle, although Unicode is usually preferred.  
  
 When reading from or writing to files, improperly matching file encodings may result in exceptions or incorrect results.  
  
## Types of Encodings  
 Unicode is the preferred encoding when working with files. Unicode is a worldwide character-encoding standard that uses 16-bit code values to represent all the characters used in modern computing, including technical symbols and special characters used in publishing.  
  
 Previous character-encoding standards consisted of traditional character sets, such as the Windows ANSI character set that uses 8-bit code values, or combinations of 8-bit values, to represent the characters used in a specific language or geographical region.  
  
## Encoding Class  
 The <xref:System.Text.Encoding?qualifyHint=False> class represents a character encoding. This table lists the type of encodings available and describes each.  
  
|||  
|-|-|  
|Name|Description|  
|<xref:System.Text.ASCIIEncoding?qualifyHint=False>|Represents an ASCII character encoding of Unicode characters.|  
|<xref:System.Text.UnicodeEncoding?qualifyHint=False>|Represents a UTF-16 encoding of Unicode characters.|  
|<xref:System.Text.UTF32Encoding?qualifyHint=False>|Represents a UTF-32 encoding of Unicode characters.|  
|<xref:System.Text.UTF7Encoding?qualifyHint=False>|Represents a UTF-7 encoding of Unicode characters.|  
|<xref:System.Text.UTF8Encoding?qualifyHint=False>|Represents a UTF-8 encoding of Unicode characters.|  
  
## See Also  
 [Reading from Files in Visual Basic](../Topic/Reading%20from%20Files%20in%20Visual%20Basic.md)   
 [Writing to Files in Visual Basic](../Topic/Writing%20to%20Files%20in%20Visual%20Basic.md)