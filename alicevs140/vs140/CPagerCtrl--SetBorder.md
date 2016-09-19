---
title: "CPagerCtrl::SetBorder"
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
ms.assetid: 92e29ddc-0fa1-445a-87cd-447a9ef0cd61
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::SetBorder
Sets the border size of the current pager control.  
  
## Syntax  
  
```  
int SetBorder(  
    int iBorder  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iBorder`|The new border size, measured in pixels. If the `iBorder` parameter is negative, the border size is set to zero.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Return Value  
 The previous border size, measured in pixels.  
  
## Remarks  
 This method sends the [PGM_SETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760880) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following example creates a pager control, then uses the [CPagerCtrl::SetChild](../vs140/CPagerCtrl--SetChild.md) method to associate a very long button control with the pager control. The example then uses the [CPagerCtrl::SetButtonSize](../vs140/CPagerCtrl--SetButtonSize.md) method to set the height of the pager control to 20 pixels, and the [CPagerCtrl::SetBorder](../vs140/CPagerCtrl--SetBorder.md) method to set the border thickness to 1 pixel.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#1)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_SETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760880)   
 [CPagerCtrl::GetBorder](../vs140/CPagerCtrl--GetBorder.md)