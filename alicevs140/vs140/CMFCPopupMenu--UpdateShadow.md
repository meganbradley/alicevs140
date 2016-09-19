---
title: "CMFCPopupMenu::UpdateShadow"
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
ms.assetid: 11ac89ce-3f7e-445e-8544-68f3143f0776
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::UpdateShadow
Updates the shadow for the pop-up menu.  
  
## Syntax  
  
```  
void UpdateShadow(  
   LPRECT lprectScreen = NULL  
);  
```  
  
#### Parameters  
 [in] `lprectScreen`  
 A rectangle, in screen coordinates, that specifies the boundaries of the region to update.  
  
## Remarks  
 Call this method when a pop-up menu that has a shadow overlaps an animated image.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)