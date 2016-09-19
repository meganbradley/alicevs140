---
title: "CWnd::OnEnterMenuLoop"
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
ms.assetid: 35220fc1-6384-41ad-9663-3546266cac10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnEnterMenuLoop
The framework calls this member function when a menu modal loop has been entered.  
  
## Syntax  
  
```  
  
      afx_msg void OnEnterMenuLoop(  
   BOOL bIsTrackPopupMenu   
);  
```  
  
#### Parameters  
 `bIsTrackPopupMenu`  
 Specifies whether the menu involved is a popup menu. Has a nonzero value if the function is successful; otherwise 0.  
  
## Remarks  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnExitMenuLoop](../vs140/CWnd--OnExitMenuLoop.md)   
 [WM_ENTERMENULOOP](http://msdn.microsoft.com/library/windows/desktop/ms647595)