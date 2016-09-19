---
title: "CToolBarCtrl::GetPadding"
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
ms.assetid: ab049e48-fb6b-463c-b976-ebafc29af842
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetPadding
Retrieves the horizontal and vertical padding of the current toolbar control.  
  
## Syntax  
  
```  
BOOL GetPadding(  
     int* pnHorzPadding,   
     int* pnVertPadding  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `pnHorzPadding`|An integer that receives the horizontal padding of the toolbar control, in pixels.|  
|[out] `pnVertPadding`|An integer that receives the vertical padding of the toolbar control, in pixels.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [TB_GETPADDING](http://msdn.microsoft.com/library/windows/desktop/bb787344) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TB_GETPADDING](http://msdn.microsoft.com/library/windows/desktop/bb787344)   
 [CToolBarCtrl::SetPadding](../vs140/CToolBarCtrl--SetPadding.md)