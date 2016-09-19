---
title: "CWnd::OnLButtonUp"
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
ms.assetid: d1557505-2caa-4ae4-b52a-207e9adf099a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnLButtonUp
The framework calls this member function when the user releases the left mouse button.  
  
## Syntax  
  
```  
  
      afx_msg void OnLButtonUp(  
   UINT nFlags,  
   CPoint point   
);  
```  
  
#### Parameters  
 `nFlags`  
 Indicates whether various virtual keys are down. This parameter can be any combination of the following values:  
  
-   **MK_CONTROL** Set if the CTRL key is down.  
  
-   **MK_MBUTTON** Set if the middle mouse button is down.  
  
-   **MK_RBUTTON** Set if the right mouse button is down.  
  
-   **MK_SHIFT** Set if the SHIFT key is down.  
  
 `point`  
 Specifies the x- and y-coordinate of the cursor. These coordinates are always relative to the upper-left corner of the window.  
  
## Remarks  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnLButtonDblClk](../vs140/CWnd--OnLButtonDblClk.md)   
 [CWnd::OnLButtonDown](../vs140/CWnd--OnLButtonDown.md)   
 [CWnd::OnLButtonUp](../vs140/CWnd--OnLButtonUp.md)