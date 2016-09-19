---
title: "CPagerCtrl::GetScrollPos"
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
ms.assetid: a0808848-b029-49d5-b768-868fa0719ff2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::GetScrollPos
Retrieves the scroll position of the current pager control.  
  
## Syntax  
  
```  
int GetScrollPos() const;  
```  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Return Value  
 The current scroll position, measured in pixels.  
  
## Remarks  
 This method sends the [PGM_GETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760874) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following example uses the [CPagerCtrl::GetScrollPos](../vs140/CPagerCtrl--GetScrollPos.md) method to retrieve the current scroll position of the pager control. If the pager control is not already scrolled to zero, the leftmost position, the example uses the [CPagerCtrl::SetScrollPos](../vs140/CPagerCtrl--SetScrollPos.md) method to set the scroll position to zero.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#7)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_GETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760874)   
 [CPagerCtrl::SetScrollPos](../vs140/CPagerCtrl--SetScrollPos.md)