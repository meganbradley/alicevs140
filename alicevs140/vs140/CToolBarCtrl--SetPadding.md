---
title: "CToolBarCtrl::SetPadding"
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
ms.assetid: 3bc1be70-6fd2-491e-a75e-52c62cad43c5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetPadding
Sets the horizontal and vertical padding of the current toolbar control.  
  
## Syntax  
  
```  
DWORD SetPadding(  
      int nHorzPadding,   
      int nVertPadding  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nHorzPadding`|Specifies the horizontal padding of the toolbar control, in pixels.|  
|[in] `nVertPadding`|Specifies the vertical padding of the toolbar control, in pixels.|  
  
## Return Value  
 A `DWORD` whose low word contains the previous horizontal padding value, and whose high word contains the previous vertical padding value. The padding values are measured in pixels.  
  
## Remarks  
 This method sends the [TB_SETPADDING](http://msdn.microsoft.com/library/windows/desktop/bb787448) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example sets the horizontal and vertical padding of the current toolbar control to 20 pixels.  
  
 [!CODE [NVC_MFC_CToolBarCtrl_s1#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CToolbarCtrl_s1#4)]  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TB_SETPADDING](http://msdn.microsoft.com/library/windows/desktop/bb787448)   
 [CToolBarCtrl::GetPadding](../vs140/CToolBarCtrl--GetPadding.md)