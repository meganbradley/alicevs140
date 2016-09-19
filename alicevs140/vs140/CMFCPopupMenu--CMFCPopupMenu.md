---
title: "CMFCPopupMenu::CMFCPopupMenu"
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
ms.assetid: 24d19699-25bf-4085-b270-dc34c6a9b139
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::CMFCPopupMenu
Constructs a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object.  
  
## Syntax  
  
```  
CMFCPopupMenu(  
   CMFCToolBarsMenuPropertyPage* pCustPage,  
   LPCTSTR lpszTitle   
);  
```  
  
#### Parameters  
 [in] `pCustPage`  
 A pointer to a customization page.  
  
 [in] `lpszTitle`  
 A string that contains the menu caption.  
  
## Remarks  
 This method allocates the resources for a `CMFCPopupMenu`. To create the pop-up menu item, call [CMFCPopupMenu::Create](../vs140/CMFCPopupMenu--Create.md).  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)