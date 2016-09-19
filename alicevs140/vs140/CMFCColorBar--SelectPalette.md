---
title: "CMFCColorBar::SelectPalette"
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
ms.assetid: dd48e184-6183-46ca-b83f-2c6338ea0265
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::SelectPalette
Sets the logical palette of the specified device context to the palette of the parent button of the current color bar control.  
  
## Syntax  
  
```  
CPalette* SelectPalette(  
   CDC* pDC  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pDC`|Pointer to the device context of the parent button of the current color bar control.|  
  
## Return Value  
 Pointer to the palette that is replaced by the palette of the parent button of the current color bar control.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)