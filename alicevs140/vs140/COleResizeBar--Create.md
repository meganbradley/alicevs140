---
title: "COleResizeBar::Create"
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
ms.assetid: a6db5507-822a-4def-a8fc-4b45990ba407
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleResizeBar::Create
Creates a child window and associates it with the `COleResizeBar` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE,  
   UINT nID = AFX_IDW_RESIZE_BAR   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Pointer to the parent window of the resize bar.  
  
 `dwStyle`  
 Specifies the [window style](../vs140/Window-Styles.md) attributes.  
  
 `nID`  
 The resize bar's child window ID.  
  
## Return Value  
 Nonzero if the resize bar was created; otherwise 0.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleResizeBar Class](../vs140/COleResizeBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CControlBar Class](../vs140/CControlBar-Class.md)