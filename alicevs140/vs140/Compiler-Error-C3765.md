---
title: "Compiler Error C3765"
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
ms.topic: error-reference
ms.assetid: feadee7a-fcfb-402c-af2f-0e656f814a13
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3765
'event': cannot define an event in a class/struct 'type' marked as an event_receiver  
  
 If a class is marked with the [event_receiver](../vs140/event_receiver.md) attribute, the class cannot contain an [__event](../vs140/__event.md) declaration.  
  
 The following sample generates C3765:  
  
```  
// C3765.cpp  
[event_receiver(native)]  
struct ER2 {  
   __event void f();   // C3765  
   __event void b(int);   // C3765  
};  
```