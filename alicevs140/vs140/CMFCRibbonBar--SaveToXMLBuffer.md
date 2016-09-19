---
title: "CMFCRibbonBar::SaveToXMLBuffer"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a7cfa890-b121-4d2f-a4ba-5d94f0885dba
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::SaveToXMLBuffer
Saves the Ribbon Bar to a buffer.  
  
## Syntax  
  
```  
UINT SaveToXMLBuffer(  
   LPBYTE* ppBuffer  
) const;  
```  
  
#### Parameters  
 `ppBuffer`  
 When this function returns, `ppBuffer` points to a buffer allocated by this method and contains Ribbon Bar information in XML format.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)