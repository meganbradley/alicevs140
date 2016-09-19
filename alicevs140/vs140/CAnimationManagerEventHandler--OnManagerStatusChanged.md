---
title: "CAnimationManagerEventHandler::OnManagerStatusChanged"
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
ms.assetid: b046e687-7794-4ea5-84c4-7a76a365af46
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationManagerEventHandler::OnManagerStatusChanged
[!INCLUDE[dev10_sp1required](../vs140/includes/dev10_sp1required_md.md)]  
  
 Called when a status of animation manager has changed.  
  
## Syntax  
  
```  
IFACEMETHOD(  
   OnManagerStatusChanged  
)(UI_ANIMATION_MANAGER_STATUS newStatus,UI_ANIMATION_MANAGER_STATUS previousStatus);  
```  
  
#### Parameters  
 `newStatus`  
 New status.  
  
 `previousStatus`  
 Previous status.  
  
## Return Value  
 Current implementation always returns S_OK;  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationManagerEventHandler Class](../vs140/CAnimationManagerEventHandler-Class.md)