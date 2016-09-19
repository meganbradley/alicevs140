---
title: "COleControlSite::ModifyStyle"
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
ms.assetid: 7858f5b7-6ae6-40a9-9b77-d8f3e6cd5a71
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::ModifyStyle
Modifies the styles of the control.  
  
## Syntax  
  
```  
  
      virtual BOOL ModifyStyle(  
   DWORD dwRemove,  
   DWORD dwAdd,  
   UINT nFlags   
);  
```  
  
#### Parameters  
 `dwRemove`  
 The styles to be removed from the current window styles.  
  
 `dwAdd`  
 The styles to be added from the current window styles.  
  
 `nFlags`  
 Window positioning flags. For a list of possible values, see the [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if the styles are changed, otherwise zero.  
  
## Remarks  
 The control's stock Enabled property will be modified to match the setting for **WS_DISABLED**. The control's stock Border Style property will be modified to match the requested setting for `WS_BORDER`. All other styles are applied directly to the control's window handle, if one is present.  
  
 Modifies the window styles of the control. Styles to be added or removed can be combined by using the bitwise OR ( &#124; ) operator. See the [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for information about the available window styles.  
  
 If `nFlags` is nonzero, `ModifyStyle` calls the Win32 function `SetWindowPos`, and redraws the window by combining `nFlags` with the following four flags:  
  
-   `SWP_NOSIZE` Retains the current size.  
  
-   `SWP_NOMOVE` Retains the current position.  
  
-   `SWP_NOZORDER` Retains the current Z order.  
  
-   `SWP_NOACTIVATE` Does not activate the window.  
  
 To modify a window's extended styles, call [ModifyStyleEx](../vs140/COleControlSite--ModifyStyleEx.md).  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)