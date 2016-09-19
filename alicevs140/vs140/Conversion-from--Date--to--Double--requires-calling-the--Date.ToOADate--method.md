---
title: "Conversion from &#39;Date&#39; to &#39;Double&#39; requires calling the &#39;Date.ToOADate&#39; method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8171ce21-e4f6-4e75-b7e8-32baf78a40eb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion from &#39;Date&#39; to &#39;Double&#39; requires calling the &#39;Date.ToOADate&#39; method
You have attempted to cast a `Date` value to a `Double` value, which cannot be done without using the <xref:System.DateTime.ToOADate?qualifyHint=True> method.  
  
 **Error ID:** BC30532  
  
### To correct this error  
  
-   Use the <xref:System.DateTime.ToOADate?qualifyHint=True> method to convert the value.  
  
## See Also  
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)