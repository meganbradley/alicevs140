---
title: "How to: Convert an Array of Bytes into a String in Visual Basic"
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
ms.assetid: d0dc8317-9ab3-4324-99f7-3f5788c0e72a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert an Array of Bytes into a String in Visual Basic
This topic shows how to convert the bytes from a byte array into a string.  
  
## Example  
 This example uses the <xref:System.Text.Encoding.GetString?qualifyHint=False> method of the <xref:System.Text.Encoding.Unicode?qualifyHint=True> encoding class to convert all the bytes from a byte array into a string.  
  
 [!CODE [VbVbalrStrings#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#72)]  
  
 You can choose from several encoding options to convert a byte array into a string:  
  
-   <xref:System.Text.Encoding.ASCII?qualifyHint=True>: Gets an encoding for the ASCII (7-bit) character set.  
  
-   <xref:System.Text.Encoding.BigEndianUnicode?qualifyHint=True>: Gets an encoding for the UTF-16 format using the big-endian byte order.  
  
-   <xref:System.Text.Encoding.Default?qualifyHint=True>: Gets an encoding for the system's current ANSI code page.  
  
-   <xref:System.Text.Encoding.Unicode?qualifyHint=True>: Gets an encoding for the UTF-16 format using the little-endian byte order.  
  
-   <xref:System.Text.Encoding.UTF32?qualifyHint=True>: Gets an encoding for the UTF-32 format using the little-endian byte order.  
  
-   <xref:System.Text.Encoding.UTF7?qualifyHint=True>: Gets an encoding for the UTF-7 format.  
  
-   <xref:System.Text.Encoding.UTF8?qualifyHint=True>: Gets an encoding for the UTF-8 format.  
  
## See Also  
 <xref:System.Text.Encoding?qualifyHint=True>   
 <xref:System.Text.Encoding.GetString?qualifyHint=False>   
 [How to: Convert Strings into an Array of Bytes in Visual Basic](../Topic/How%20to:%20Convert%20Strings%20into%20an%20Array%20of%20Bytes%20in%20Visual%20Basic.md)