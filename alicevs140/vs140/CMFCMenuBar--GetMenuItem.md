---
title: "CMFCMenuBar::GetMenuItem"
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
ms.assetid: 982ec91a-4830-4c68-90af-5ee05328899a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::GetMenuItem
Retrieves a [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) object on a menu bar based on the item index.  
  
## Syntax  
  
```  
CMFCToolBarButton* GetMenuItem(  
   int iItem  
) const;  
```  
  
#### Parameters  
 [in] `iItem`  
 The index of the menu item to return.  
  
## Return Value  
 A pointer to the `CMFCToolBarButton` object that matches the index specified by `iItem`. `NULL` if the index is invalid.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)