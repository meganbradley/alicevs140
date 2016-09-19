---
title: "CWnd::OnMoving"
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
ms.assetid: 0f2dc2d2-5812-4840-97f1-dcf48e2d76ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnMoving
The framework calls this member function while a user is moving a `CWnd` object.  
  
## Syntax  
  
```  
  
      afx_msg void OnMoving(  
   UINT nSide,  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `nSide`  
 The edge of window to be moved.  
  
 `lpRect`  
 Address of the [CRect](../vs140/CRect-Class.md) or [RECT](../vs140/RECT-Structure.md) structure that will contain the item's coordinates.  
  
## Remarks  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnMove](../vs140/CWnd--OnMove.md)