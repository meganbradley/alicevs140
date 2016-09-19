---
title: "CMFCMenuBar::CreateFromMenu"
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
ms.assetid: bea22436-4b0d-488e-ad58-3290a27a62af
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::CreateFromMenu
Initializes a [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object. This method models the `CMFCMenuBar` object after a `HMENU` parameter.  
  
## Syntax  
  
```  
virtual void CreateFromMenu(  
   HMENU hMenu,  
   BOOL bDefaultMenu = FALSE,  
   BOOL bForceUpdate = FALSE  
);  
```  
  
#### Parameters  
 [in] `hMenu`  
 A handle to a menu resource. `CreateFromMenu` uses this resource as a template for the `CMFCMenuBar`.  
  
 [in] `bDefaultMenu`  
 A Boolean that indicates whether the new menu is the default menu.  
  
 [in] `bForceUpdate`  
 A Boolean that indicates whether this method forces a menu update.  
  
## Remarks  
 Use this method if you want a menu control to have the same menu items as a menu resource. You call this method after you call either [CMFCMenuBar::Create](../vs140/CMFCMenuBar--Create.md) or [CMFCMenuBar::CreateEx](../vs140/CMFCMenuBar--CreateEx.md).  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)