---
title: "CRichEditCtrl::StopGroupTyping"
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
ms.assetid: dc4b1c1e-97f2-4dc3-9ff9-17e676adf54f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::StopGroupTyping
Stops the control from collecting additional typing actions into the current undo action.  
  
## Syntax  
  
```  
  
void StopGroupTyping( );  
  
```  
  
## Remarks  
 The control stores the next typing action, if any, into a new action in the undo queue.  
  
 For more information, see [EM_STOPGROUPTYPING](http://msdn.microsoft.com/library/windows/desktop/bb774300) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)