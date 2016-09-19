---
title: "CMFCColorPopupMenu::CreateTearOffBar"
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
ms.assetid: 48d8d08e-4b5d-452c-bd3a-89c5588e43ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorPopupMenu::CreateTearOffBar
Creates a dockable tear-off color bar.  
  
## Syntax  
  
```  
virtual CPane* CreateTearOffBar(  
   CFrameWnd* pWndMain,  
   UINT uiID,  
   LPCTSTR lpszName  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pWndMain`|Pointer to the parent window of the tear-off bar.|  
|[in] `uiID`|The command ID of the tear-off bar.|  
|[in] `lpszName`|The window text of the tear-off bar.|  
  
## Return Value  
 A pointer to the new tear-off control bar object.  
  
## Remarks  
 This method creates a [CMFCColorBar](../vs140/CMFCColorBar-Class.md) object and casts it to a [CPane](../vs140/CPane-Class.md) pointer. You can cast this value back to a [CMFCColorBar](../vs140/CMFCColorBar-Class.md) pointer by using one of the casting macros described in [Type Casting of MFC Class Objects](../vs140/Type-Casting-of-MFC-Class-Objects.md).  
  
## Requirements  
 **Header:** afxcolorpopupmenu.h  
  
## See Also  
 [CMFCColorPopupMenu Class](../vs140/CMFCColorPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [CMFCColorBar](../vs140/CMFCColorBar-Class.md)   
 [Type Casting of MFC Class Objects](../vs140/Type-Casting-of-MFC-Class-Objects.md)