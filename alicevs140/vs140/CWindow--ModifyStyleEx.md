---
title: "CWindow::ModifyStyleEx"
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
ms.assetid: 2f1b61d9-cb9c-4fc7-8a36-4c086ffbb6c2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ModifyStyleEx
Modifies the extended window styles of the `CWindow` object.  
  
## Syntax  
  
```  
  
      BOOL ModifyStyleEx(  
   DWORD dwRemove,  
   DWORD dwAdd,  
   UINT nFlags = 0   
) throw();  
```  
  
#### Parameters  
 `dwRemove`  
 [in] Specifies the extended styles to be removed during style modification.  
  
 `dwAdd`  
 [in] Specifies the extended styles to be added during style modification.  
  
 `nFlags`  
 [in] Window-positioning flags. For a list of possible values, see the [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 **TRUE** if the extended window styles are modified; otherwise, **FALSE**.  
  
## Remarks  
 Styles to be added or removed can be combined by using the bitwise OR ( &#124; ) operator. See the [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]for information about the available extended styles.  
  
 If `nFlags` is nonzero, `ModifyStyleEx` calls the Win32 function `SetWindowPos`, and redraws the window by combining `nFlags` with the following four flags:  
  
-   `SWP_NOSIZE` Retains the current size.  
  
-   `SWP_NOMOVE` Retains the current position.  
  
-   `SWP_NOZORDER` Retains the current Z order.  
  
-   `SWP_NOACTIVATE` Does not activate the window.  
  
 To modify windows using regular window styles, call [ModifyStyle](../vs140/CWindow--ModifyStyle.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#26](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#26)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetExStyle](../vs140/CWindow--GetExStyle.md)