---
title: "CAnimationVariableIntegerChangeHandler::OnIntegerValueChanged"
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
ms.assetid: 94196e52-e66e-4ed8-824d-f5ad19a633cb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariableIntegerChangeHandler::OnIntegerValueChanged
Called when a value of an animation variable has changed.  
  
## Syntax  
  
```  
IFACEMETHOD(  
   OnIntegerValueChanged  
) ( __in IUIAnimationStoryboard *storyboard, __in IUIAnimationVariable *variable, __in INT32 newValue, __in INT32 previousValue );  
```  
  
#### Parameters  
 `storyboard`  
 The storyboard that is animating the variable.  
  
 `variable`  
 The animation variable that was updated.  
  
 `newValue`  
 The new rounded value.  
  
 `previousValue`  
 The previous rounded value.  
  
## Return Value  
 S_OK if the method succeeds; otherwise E_FAIL.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariableIntegerChangeHandler Class](../vs140/CAnimationVariableIntegerChangeHandler-Class.md)