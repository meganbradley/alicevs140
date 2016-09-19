---
title: "CPaneFrameWnd::CreateEx"
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
ms.assetid: 060f11a6-f62a-45d2-a0c9-fb90b41df66c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::CreateEx
Creates a miniframe window and attaches it to the [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md) object.  
  
## Syntax  
  
```  
virtual BOOL CreateEx(  
   DWORD dwStyleEx,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   CCreateContext* pContext=NULL   
);  
```  
  
#### Parameters  
 [in] `dwStyleEx`  
 Specifies the extended window style. For more information, see [Extended Window Styles](../vs140/Extended-Window-Styles.md)  
  
 [in] `lpszWindowName`  
 Specifies the text to display on the miniframe window.  
  
 [in] `dwStyle`  
 Specifies the window style. For more information, see [Window Styles](../vs140/Window-Styles.md).  
  
 [in] `rect`  
 Specifies the initial size and position of the miniframe window.  
  
 [in] [out] `pParentWnd`  
 Specifies the parent frame of the miniframe window. This value must not be `NULL`.  
  
 [in] [out] `pContext`  
 Specifies user-defined context.  
  
## Return Value  
 `TRUE` if the window was created successfully; otherwise, `FALSE`.  
  
## Remarks  
 A miniframe window is created in two steps. First, the framework creates a [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md) object. Second, it calls `Create` to create the Windows miniframe window and attach it to the `CPaneFrameWnd` object.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)