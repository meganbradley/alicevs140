---
title: "CPagerCtrl::SetBkColor"
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
ms.assetid: 97350564-049d-4cf2-a882-7f8a5b92ec2e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::SetBkColor
Sets the background color of the current pager control.  
  
## Syntax  
  
```  
COLORREF SetBkColor(  
         COLORREF clrBk  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `clrBk`|A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that contains the new background color of the pager control.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that contains the previous background color of the pager control.  
  
## Remarks  
 This method sends the [PGM_SETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760878) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following example uses the [CPagerCtrl::SetBkColor](../vs140/CPagerCtrl--SetBkColor.md) method to set the background color of the pager control to red, and the [CPagerCtrl::GetBkColor](../vs140/CPagerCtrl--GetBkColor.md) method to confirm that the change was made.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#4)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_SETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760878)   
 [CPagerCtrl::GetBkColor](../vs140/CPagerCtrl--GetBkColor.md)