---
title: "CScrollBar::SetScrollInfo"
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
ms.assetid: c560387a-4f8a-4650-99eb-ce695df9e797
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::SetScrollInfo
Sets the information that the `SCROLLINFO` structure maintains about a scroll bar.  
  
## Syntax  
  
```  
  
      BOOL SetScrollInfo(  
   LPSCROLLINFO lpScrollInfo,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `lpScrollInfo`  
 A pointer to a [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537) structure.  
  
 `bRedraw`  
 Specifies whether the scroll bar should be redrawn to reflect the new information. If `bRedraw` is **TRUE**, the scroll bar is redrawn. If it is **FALSE**, it is not redrawn. The scroll bar is redrawn by default.  
  
## Return Value  
 If successful, the return is **TRUE**. Otherwise, it is **FALSE**.  
  
## Remarks  
 You must provide the values required by the `SCROLLINFO` structure parameters, including the flag values.  
  
 The `SCROLLINFO` structure contains information about a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (the thumb). See the [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537) structure topic in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about changing the structure defaults.  
  
## Example  
 [!CODE [NVC_MFC_CScrollBar#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CScrollBar#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::GetScrollInfo](../vs140/CScrollBar--GetScrollInfo.md)   
 [CWnd::SetScrollInfo](../vs140/CWnd--SetScrollInfo.md)   
 [CWnd::SetScrollPos](../vs140/CWnd--SetScrollPos.md)   
 [CWnd::OnVScroll](../vs140/CWnd--OnVScroll.md)   
 [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md)   
 [CWnd::GetScrollInfo](../vs140/CWnd--GetScrollInfo.md)   
 [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537)