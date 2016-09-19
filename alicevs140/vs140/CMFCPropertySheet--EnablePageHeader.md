---
title: "CMFCPropertySheet::EnablePageHeader"
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
ms.assetid: eb594dba-952d-43a5-8270-042064105c78
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::EnablePageHeader
Reserves space at the top of each page to draw a custom header.  
  
## Syntax  
  
```  
void EnablePageHeader(  
   int nHeaderHeight   
);  
```  
  
#### Parameters  
 [in] `nHeaderHeight`  
 The height of the header, in pixels.  
  
## Remarks  
 To use the value of the `nHeaderHeight` parameter to draw a custom header, override the [CMFCPropertySheet::OnDrawPageHeader](../vs140/CMFCPropertySheet--OnDrawPageHeader.md) method.  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertySheet::OnDrawPageHeader](../vs140/CMFCPropertySheet--OnDrawPageHeader.md)   
 [CMFCPropertySheet::GetHeaderHeight](../vs140/CMFCPropertySheet--GetHeaderHeight.md)