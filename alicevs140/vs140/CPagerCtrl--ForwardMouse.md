---
title: "CPagerCtrl::ForwardMouse"
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
ms.assetid: 6fd36fd2-ba70-45cb-8075-f76c57c73e25
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::ForwardMouse
Enables or disables forwarding [WM_MOUSEMOVE](http://msdn.microsoft.com/library/windows/desktop/ms645616) messages to the window that is contained in the current pager control.  
  
## Syntax  
  
```  
void ForwardMouse(  
     BOOL bForward  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `bForward`|`true` to forward mouse messages, or `false` to not forward mouse messages.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 This method sends the [PGM_FORWARDMOUSE](http://msdn.microsoft.com/library/windows/desktop/bb760867) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_FORWARDMOUSE](http://msdn.microsoft.com/library/windows/desktop/bb760867)   
 [WM_MOUSEMOVE](http://msdn.microsoft.com/library/windows/desktop/ms645616)