---
title: "CWnd::EnableToolTips"
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
ms.assetid: 186b5b14-c000-4492-84f0-9ec83cf5b63f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::EnableToolTips
Enables tool tips for the given window.  
  
## Syntax  
  
```  
  
      BOOL EnableToolTips(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether the tool tip control is enabled or disabled. **TRUE** enables the control; **FALSE** disables the control.  
  
## Return Value  
 **TRUE** if tool tips are enabled; otherwise **FALSE**.  
  
## Remarks  
 Override [OnToolHitTest](../vs140/CWnd--OnToolHitTest.md) to provide the [TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256) struct or structs for the window.  
  
> [!NOTE]
>  Some windows, such as [CToolBar](../vs140/CToolBar-Class.md), provide a built-in implementation of [OnToolHitTest](../vs140/CWnd--OnToolHitTest.md).  
  
 See [TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on this structure.  
  
 Simply calling `EnableToolTips` is not enough to display tool tips for your child controls unless the parent window is derived from `CFrameWnd`. This is because `CFrameWnd` provides a default handler for the **TTN_NEEDTEXT** notification. If your parent window is not derived from `CFrameWnd`, that is, if it is a dialog box or a form view, tool tips for your child controls will not display correctly unless you provide a handler for the **TTN_NEEDTEXT** tool tip notification. See [Tool Tips](../vs140/Tool-Tips-in-Windows-Not-Derived-from-CFrameWnd.md).  
  
 The default tool tips provided for your windows by `EnableToolTips` do not have text associated with them. To retrieve text for the tool tip to display, the **TTN_NEEDTEXT** notification is sent to the tool tip control's parent window just before the tool tip window is displayed. If there is no handler for this message to assign some value to the `pszText` member of the **TOOLTIPTEXT** structure, there will be no text displayed for the tool tip.  
  
## Example  
 [!CODE [NVC_MFCWindowing#91](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#91)]  
  
 [!CODE [NVC_MFCWindowing#92](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#92)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::CancelToolTips](../vs140/CWnd--CancelToolTips.md)   
 [CWnd::OnToolHitTest](../vs140/CWnd--OnToolHitTest.md)   
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)