---
title: "CPagerCtrl::SetChild"
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
ms.assetid: 8870116a-541e-4d0e-9424-383c71ad8b63
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::SetChild
Sets the contained window for the current pager control.  
  
## Syntax  
  
```  
void SetChild(  
     HWND hwndChild  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `hwndChild`|Handle to the window to be contained.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 This method sends the [PGM_SETCHILD](http://msdn.microsoft.com/library/windows/desktop/bb760884) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 This method does not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling. In most cases, the contained window will be a child window of the pager control.  
  
## Example  
 The following example creates a pager control, then uses the [CPagerCtrl::SetChild](../vs140/CPagerCtrl--SetChild.md) method to associate a very long button control with the pager control. The example then uses the [CPagerCtrl::SetButtonSize](../vs140/CPagerCtrl--SetButtonSize.md) method to set the height of the pager control to 20 pixels, and the [CPagerCtrl::SetBorder](../vs140/CPagerCtrl--SetBorder.md) method to set the border thickness to 1 pixel.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#1)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)