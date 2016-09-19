---
title: "CMFCMenuButton::SizeToContent"
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
ms.assetid: d5da7a2c-918c-45e7-b088-cbafce973acf
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuButton::SizeToContent
Changes the size of the button according to its text size and image size.  
  
## Syntax  
  
```  
virtual CSize SizeToContent(  
   BOOL bCalcOnly = FALSE  
);  
```  
  
#### Parameters  
 [in] `bCalcOnly`  
 A Boolean parameter that indicates whether this method resizes the button .  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that specifies the new size for the button.  
  
## Remarks  
 If you call this function and `bCalcOnly` is `TRUE`, `SizeToContent` will calculate only the new size of the button.  
  
 The new size of the button is calculated to fit the button text, image, and arrow. The framework also adds in predefined margins of 10 pixels for the horizontal edge and 5 pixels for the vertical edge.  
  
## Requirements  
 **Header:** afxmenubutton.h  
  
## See Also  
 [CMFCMenuButton Class](../vs140/CMFCMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)