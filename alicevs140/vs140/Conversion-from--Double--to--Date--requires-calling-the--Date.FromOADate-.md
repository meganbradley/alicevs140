---
title: "Conversion from &#39;Double&#39; to &#39;Date&#39; requires calling the &#39;Date.FromOADate&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: afcfd115-4614-4b0b-ad09-76af8dba2ed5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion from &#39;Double&#39; to &#39;Date&#39; requires calling the &#39;Date.FromOADate&#39;
You have attempted to cast a `Date` value to a `Double` value, which cannot be done without using the <xref:System.DateTime.FromOADate?qualifyHint=True> method.  
  
 **Error ID:** BC30533  
  
### To correct this error  
  
-   Use the <xref:System.DateTime.FromOADate?qualifyHint=False> method to convert the value.  
  
## See Also  
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)