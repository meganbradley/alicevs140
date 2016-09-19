---
title: "CMFCPopupMenu::SetForceShadow"
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
ms.assetid: 0bbd57f6-26fb-4e07-bbae-5efb527bb1ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::SetForceShadow
Forces the framework to draw menu shadows when pop-up menus appear outside the main frame.  
  
## Syntax  
  
```  
static void SetForceShadow(  
   BOOL bValue   
);  
```  
  
#### Parameters  
 [in] `bValue`  
 `TRUE` if you want the framework to draw menu shadows, `FALSE` otherwise.  
  
## Remarks  
 When you call this method, it sets a global flag in your application. This flag affects all pop-up menus in your application.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)