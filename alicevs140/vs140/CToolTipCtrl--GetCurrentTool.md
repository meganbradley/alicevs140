---
title: "CToolTipCtrl::GetCurrentTool"
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
ms.assetid: fb14e47b-4167-4e82-a4ae-a59ca78e1aea
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::GetCurrentTool
Retrieves information, such as the size, position, and text, of the tooltip window displayed by the current tooltip control.  
  
## Syntax  
  
```  
BOOL GetCurrentTool(  
     LPTOOLINFO lpToolInfo  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `lpToolInfo`|Pointer to a [TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256) structure that receives information about the current tooltip window.|  
  
## Return Value  
 `true` if the information is retrieved successfully; otherwise, `false.`  
  
## Remarks  
 This method sends the [TTM_GETCURRENTTOOL](http://msdn.microsoft.com/library/windows/desktop/bb760389) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example retrieves information about the current tooltip window.  
  
 [!CODE [NVC_MFC_CToolBarCtrl_s1#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CToolbarCtrl_s1#6)]  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TTM_GETCURRENTTOOL](http://msdn.microsoft.com/library/windows/desktop/bb760389)   
 [TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)