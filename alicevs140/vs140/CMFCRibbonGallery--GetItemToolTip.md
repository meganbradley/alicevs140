---
title: "CMFCRibbonGallery::GetItemToolTip"
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
ms.assetid: 944ceddb-6b8a-4b80-a6a2-f5c2648cf619
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::GetItemToolTip
Returns the tooltip text that is associated with an item in the gallery.  
  
## Syntax  
  
```  
LPCTSTR GetItemToolTip(  
    int nItemIndex   
) const;  
```  
  
#### Parameters  
 [in] `nItemIndex`  
 Specifies the zero-based index of the item for which to retrieve the tooltip text.  
  
## Return Value  
 A pointer to the tooltip string assigned to an item in the ribbon gallery. It can be `NULL` if no tooltip is assigned to that item.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)