---
title: "CWnd::OnStyleChanging"
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
ms.assetid: 8e0727ab-3c41-4340-bbf4-003b55105311
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnStyleChanging
The framework calls this member function when the [SetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633591) function is about to change one or more of the window's styles.  
  
## Syntax  
  
```  
  
      afx_msg void OnStyleChanging(  
   int nStyleType,  
   LPSTYLESTRUCT lpStyleStruct   
);  
```  
  
#### Parameters  
 `nStyleType`  
 Specifies whether the window's extended or nonextended styles have changed. This parameter can be a combination of the following values:  
  
-   **GWL_EXSTYLE** The window's extended styles have changed.  
  
-   **GWL_STYLE** The window's nonextended styles have changed.  
  
 `lpStyleStruct`  
 Points to a [STYLESTRUCT](http://msdn.microsoft.com/library/windows/desktop/ms632607) structure that contains the new styles for the window. An application can examine the styles and change them.  
  
## Remarks  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)