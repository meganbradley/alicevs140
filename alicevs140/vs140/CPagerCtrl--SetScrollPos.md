---
title: "CPagerCtrl::SetScrollPos"
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
ms.assetid: 5365a2b7-568e-41e0-8c88-2ef6612d4939
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::SetScrollPos
Sets the scroll position of the current pager control.  
  
## Syntax  
  
```  
void SetScrollPos(  
     int iPos  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iPos`|The new scroll position, measured in pixels.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 This method sends the [PGM_SETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760886) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_SETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760886)   
 [CPagerCtrl::GetScrollPos](../vs140/CPagerCtrl--GetScrollPos.md)