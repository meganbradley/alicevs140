---
title: "CMFCRibbonBaseElement::GetCompactSize"
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
ms.assetid: dd8fa08b-d527-4141-bdce-c8a83a9cd50c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetCompactSize
Returns the compact size of the ribbon element.  
  
## Syntax  
  
```  
virtual CSize GetCompactSize(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
## Return Value  
 The compact size of a ribbon element.  
  
> [!NOTE]
>  The compact size means that the ribbon element is truncated (it displays a small image, or an image without a text).  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)