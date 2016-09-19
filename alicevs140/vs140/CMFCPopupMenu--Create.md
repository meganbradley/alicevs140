---
title: "CMFCPopupMenu::Create"
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
ms.assetid: f3c387e1-2027-4519-b55d-781a321ac602
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::Create
Creates a pop-up menu and attaches it to a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   CWnd* pWndParent,  
   int x,  
   int y,  
   HMENU hMenu,  
   BOOL bLocked = FALSE,  
   BOOL bOwnMessage = FALSE  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 The parent window for the `CMFCPopupMenu`.  
  
 [in] `x`  
 The horizontal screen coordinate for the location of the pop-up menu  
  
 [in] `y`  
 The vertical screen coordinate for the location of the pop-menu.  
  
 [in] `hMenu`  
 A handle to a menu resource.  
  
 [in] `bLocked`  
 A Boolean parameter that indicates whether the menu is customizable. `FALSE` indicates that the pop-up menu is customizable.  
  
 [in] `bOwnMessage`  
 A Boolean parameter that indicates how the framework routes the menu messages. See the Remarks section for more details.  
  
## Return Value  
 `TRUE` if the method is successful; otherwise `FALSE`.  
  
## Remarks  
 If `bOwnMessage` is `TRUE`, the framework routes any menu messages to `pWndParent`. `pWndParent` must not be `NULL` if `bOwnMessage` is `TRUE.` If `bOwnMessage` is `FALSE`, the framework routes the menu messages to the parent pop-up menu.  
  
## Example  
 The following example demonstrates how to use the `Create` method of the `CMFCPopuMenu` class. This code snippet is part of the [Custom Pages sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_CustomPages#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_CustomPages#1)]  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)