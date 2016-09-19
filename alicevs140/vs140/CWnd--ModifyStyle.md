---
title: "CWnd::ModifyStyle"
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
ms.assetid: 5b6c28bd-ec51-45c4-b7fe-a8ae522f9ba8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ModifyStyle
Call this member function to modify a window's style.  
  
## Syntax  
  
```  
  
      BOOL ModifyStyle(  
   DWORD dwRemove,  
   DWORD dwAdd,  
   UINT nFlags = 0   
);  
```  
  
#### Parameters  
 `dwRemove`  
 Specifies window styles to be removed during style modification.  
  
 `dwAdd`  
 Specifies window styles to be added during style modification.  
  
 `nFlags`  
 Flags to be passed to [SetWindowPos](../vs140/CWnd--SetWindowPos.md), or zero if `SetWindowPos` should not be called. The default is zero. See the Remarks section for a list of preset flags.  
  
## Return Value  
 Nonzero if style was successfully modified; otherwise, 0.  
  
## Remarks  
 Styles to be added or removed can be combined by using the bitwise OR (&#124;) operator. See the topics [Window Styles](http://msdn.microsoft.com/library/windows/desktop/ms632600) and [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for information about the available window styles.  
  
 If `nFlags` is nonzero, `ModifyStyle` calls the Windows API function [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) and redraws the window by combining `nFlags` with the following four preset flags:  
  
-   `SWP_NOSIZE` Retains the current size.  
  
-   `SWP_NOMOVE` Retains the current position.  
  
-   `SWP_NOZORDER` Retains the current Z order.  
  
-   `SWP_NOACTIVATE` Does not activate the window.  
  
 To modify a window's extended styles, see [ModifyStyleEx](../vs140/CWnd--ModifyStyleEx.md).  
  
> [!NOTE]
>  For some styles in certain controls (the **ES_READONLY** style in the edit control, for example), **ModifyStyle** may not properly change the style because the control may need to perform special internal processing. In these cases, a corresponding message to change the style will be available (**EM_SETREADONLY** in the example mentioned).  
  
## Example  
 [!CODE [NVC_MFCWindowing#105](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#105)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md)   
 [CWnd::ModifyStyleEx](../vs140/CWnd--ModifyStyleEx.md)   
 [Window Styles](http://msdn.microsoft.com/library/windows/desktop/ms632600)   
 [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545)