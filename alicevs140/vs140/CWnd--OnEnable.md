---
title: "CWnd::OnEnable"
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
ms.assetid: a5a63397-c8d8-485f-b287-d185a9316886
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnEnable
The framework calls this member function when an application changes the enabled state of the `CWnd` object.  
  
## Syntax  
  
```  
  
      afx_msg void OnEnable(  
   BOOL bEnable   
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether the `CWnd` object has been enabled or disabled. This parameter is **TRUE** if the `CWnd` has been enabled; it is **FALSE** if the `CWnd` has been disabled.  
  
## Remarks  
 `OnEnable` is called before the [EnableWindow](../vs140/CWnd--EnableWindow.md) member function returns, but after the window enabled state ([WS_DISABLED](../vs140/Window-Styles.md) style bit) has changed.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EnableWindow](../vs140/CWnd--EnableWindow.md)   
 [WM_ENABLE](http://msdn.microsoft.com/library/windows/desktop/ms632621)