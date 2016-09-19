---
title: "Context::CurrentContext Method"
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
ms.topic: article
ms.assetid: d57bf982-3fcf-48aa-ae01-89885f7dd8f0
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::CurrentContext Method
Returns a pointer to the current context.  
  
## Syntax  
  
```  
static Context * __cdecl CurrentContext();  
```  
  
## Return Value  
 A pointer to the current context.  
  
## Remarks  
 This method will result in the process' default scheduler being created and/or attached to the calling context if there is no scheduler currently associated with the calling context.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)