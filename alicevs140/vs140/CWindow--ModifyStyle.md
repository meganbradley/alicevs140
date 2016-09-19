---
title: "CWindow::ModifyStyle"
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
ms.assetid: 830f68de-07f4-4ce4-9b1b-6e8011ab3f43
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ModifyStyle
Modifies the window styles of the `CWindow` object.  
  
## Syntax  
  
```  
  
      BOOL ModifyStyle(  
   DWORD dwRemove,  
   DWORD dwAdd,  
   UINT nFlags = 0   
) throw();  
```  
  
#### Parameters  
 `dwRemove`  
 [in] Specifies the window styles to be removed during style modification.  
  
 `dwAdd`  
 [in] Specifies the window styles to be added during style modification.  
  
 `nFlags`  
 [in] Window-positioning flags. For a list of possible values, see the [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 **TRUE** if the window styles are modified; otherwise, **FALSE**.  
  
## Remarks  
 Styles to be added or removed can be combined by using the bitwise OR ( &#124; ) operator. See the [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]for information about the available window styles.  
  
 If `nFlags` is nonzero, `ModifyStyle` calls the Win32 function `SetWindowPos`, and redraws the window by combining `nFlags` with the following four flags:  
  
-   `SWP_NOSIZE` Retains the current size.  
  
-   `SWP_NOMOVE` Retains the current position.  
  
-   `SWP_NOZORDER` Retains the current Z order.  
  
-   `SWP_NOACTIVATE` Does not activate the window.  
  
 To modify a window's extended styles, call [ModifyStyleEx](../vs140/CWindow--ModifyStyleEx.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#25](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#25)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetStyle](../vs140/CWindow--GetStyle.md)