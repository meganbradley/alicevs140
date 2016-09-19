---
title: "CMFCRibbonSeparator::OnDrawOnList"
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
ms.assetid: 15aa765d-e807-4361-b9a6-31f16e0585b0
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonSeparator::OnDrawOnList
Called by the system to draw the separator on the **Commands** list.  
  
## Syntax  
  
```  
virtual void OnDrawOnList(  
   CDC* pDC,  
   CString strText,  
   int nTextOffset,  
   CRect rect,  
   BOOL bIsSelected,  
   BOOL bHighlighted  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pDC`|A pointer to a device context.|  
|[in] `strText`|Text displayed on the list.|  
|[in] `nTextOffset`|Spacing between the text and the left side of the bounding rectangle.|  
|[in] `rect`|Specifies the bounding rectangle.|  
|[in] `bIsSelected`|Ignored.|  
|[in] `bHighlighted`|Ignored.|  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonSeparator Class](../vs140/CMFCRibbonSeparator-Class.md)