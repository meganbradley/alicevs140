---
title: "CWnd::OnGetMinMaxInfo"
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
ms.assetid: 2a89d834-3f43-456a-a000-34a011febe68
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnGetMinMaxInfo
The framework calls this member function whenever Windows needs to know the maximized position or dimensions, or the minimum or maximum tracking size.  
  
## Syntax  
  
```  
  
      afx_msg void OnGetMinMaxInfo(   
   MINMAXINFO* lpMMI    
);  
```  
  
#### Parameters  
 *lpMMI*  
 Points to a `MINMAXINFO` structure that contains information about a window's maximized size and position and its minimum and maximum tracking size. For more about this structure, see the [MINMAXINFO](../vs140/MINMAXINFO-Structure.md) structure.  
  
## Remarks  
 The maximized size is the size of the window when its borders are fully extended. The maximum tracking size of the window is the largest window size that can be achieved by using the borders to size the window. The minimum tracking size of the window is the smallest window size that can be achieved by using the borders to size the window.  
  
 Windows fills in an array of points specifying default values for the various positions and dimensions. The application may change these values in `OnGetMinMaxInfo`.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_GETMINMAXINFO](http://msdn.microsoft.com/library/windows/desktop/ms632626)