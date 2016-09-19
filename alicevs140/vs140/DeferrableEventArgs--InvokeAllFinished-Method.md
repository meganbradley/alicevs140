---
title: "DeferrableEventArgs::InvokeAllFinished Method"
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
ms.assetid: 86b45205-3edb-4134-9cd0-ed7a7b4c3b1a
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DeferrableEventArgs::InvokeAllFinished Method
Called to indicate that all processing to handle a deferred event is complete.  
  
## Syntax  
  
```cpp  
void InvokeAllFinished()  
```  
  
## Remarks  
 You should call this method after the event source calls [InvokeAll](../vs140/EventSource--InvokeAll-Method.md). Calling this method prevents further deferrals from being taken and forces the completion handler to execute if no deferrals were taken.  
  
 For a code example, see [DeferredEventArgs Class](../vs140/DeferrableEventArgs-Class.md).  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [DeferrableEventArgs Class](../vs140/DeferrableEventArgs-Class.md)   
 [EventSource::InvokeAll](../vs140/EventSource--InvokeAll-Method.md)