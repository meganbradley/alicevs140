---
title: "CWnd::OnSize"
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
ms.assetid: b10298b1-b1fe-4db0-8ac2-ca603aa1e8a4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnSize
The framework calls this member function after the window's size has changed.  
  
## Syntax  
  
```  
  
      afx_msg void OnSize(  
   UINT nType,  
   int cx,  
   int cy   
);  
```  
  
#### Parameters  
 `nType`  
 Specifies the type of resizing requested. This parameter can be one of the following values:  
  
-   **SIZE_MAXIMIZED** Window has been maximized.  
  
-   **SIZE_MINIMIZED** Window has been minimized.  
  
-   **SIZE_RESTORED** Window has been resized, but neither **SIZE_MINIMIZED** nor **SIZE_MAXIMIZED** applies.  
  
-   **SIZE_MAXHIDE** Message is sent to all pop-up windows when some other window is maximized.  
  
-   **SIZE_MAXSHOW** Message is sent to all pop-up windows when some other window has been restored to its former size.  
  
 `cx`  
 Specifies the new width of the client area.  
  
 `cy`  
 Specifies the new height of the client area.  
  
## Remarks  
 If the [SetScrollPos](../vs140/CWnd--SetScrollPos.md) or [MoveWindow](../vs140/CWnd--MoveWindow.md) member function is called for a child window from `OnSize`, the `bRedraw` parameter of `SetScrollPos` or `MoveWindow` should be nonzero to cause the `CWnd` to be repainted.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#109](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#109)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::MoveWindow](../vs140/CWnd--MoveWindow.md)   
 [CWnd::SetScrollPos](../vs140/CWnd--SetScrollPos.md)   
 [WM_SIZE](http://msdn.microsoft.com/library/windows/desktop/ms632646)