---
title: "CWinAppEx::OnViewDoubleClick"
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
ms.assetid: 69016ffe-7a82-4ec2-aa16-5be455cfe890
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::OnViewDoubleClick
Calls the user-defined command that is associated with a view when the user double-clicks anywhere within that view.  
  
## Syntax  
  
```  
virtual BOOL OnViewDoubleClick(  
   CWnd* pWnd,  
   int iViewId   
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 A pointer to an object derived from the [CView Class](../vs140/CView-Class.md).  
  
 [in] `iViewId`  
 The view ID.  
  
## Return Value  
 `True` if the framework finds a command; otherwise false.  
  
## Remarks  
 In order to support custom mouse behavior, you must call this function when you process the `WM_LBUTTONDBLCLK` message. This method will execute the command associated with the view ID supplied by `iViewId`. For more information about custom mouse behavior, see [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md).  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md)