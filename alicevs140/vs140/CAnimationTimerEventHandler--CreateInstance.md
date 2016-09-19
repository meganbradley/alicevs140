---
title: "CAnimationTimerEventHandler::CreateInstance"
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
ms.assetid: 2bf17cc1-9d3d-4c77-9d1a-733feebca754
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationTimerEventHandler::CreateInstance
Creates an instance of CAnimationTimerEventHandler callback.  
  
## Syntax  
  
```  
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(  
   CAnimationController* pAnimationController,  
   IUIAnimationTimerEventHandler **ppTimerEventHandler  
);  
```  
  
#### Parameters  
 `pAnimationController`  
 A pointer to animation controller, which will receive events.  
  
 `ppTimerEventHandler`  
  
## Return Value  
 If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationTimerEventHandler Class](../vs140/CAnimationTimerEventHandler-Class.md)