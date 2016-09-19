---
title: "CPagerCtrl::IsButtonInvisible"
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
ms.assetid: 54ff56ca-2595-46ad-9d92-0452616fbf06
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::IsButtonInvisible
Indicates whether the specified scroll button of the current pager control is in invisible state.  
  
## Syntax  
  
```  
BOOL IsButtonInvisible(  
     int iButton  
) const;  
```  
  
## Requirements  
 **Header:** afxcmn.h  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iButton`|Indicates the button for which the state is retrieved. If the pager control style is `PGS_HORZ`, specify `PGB_TOPORLEFT` for the left button and `PGB_BOTTOMORRIGHT` for the right button. If the pager control style is `PGS_VERT`, specify `PGB_TOPORLEFT` for the top button and `PGB_BOTTOMORRIGHT` for the bottom button. For more information, see [Pager Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760859).|  
  
## Return Value  
 `true` if the specified button is in invisible state; otherwise, `false`.  
  
## Remarks  
 Windows makes the scroll button in a particular direction invisible when the contained window is scrolled to its farthest extent because clicking the button further cannot bring more of the contained window into view.  
  
 This method sends the [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. It then tests whether the state that is returned is `PGF_INVISIBLE`. For more information, see the Return Value section of the [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) message.  
  
## Example  
 The following example uses the [CPagerCtrl::IsButtonInvisible](../vs140/CPagerCtrl--IsButtonInvisible.md) method to determine whether the pager control's left and right scroll buttons are visible.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#6)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871)   
 [CPagerCtrl::GetButtonState](../vs140/CPagerCtrl--GetButtonState.md)