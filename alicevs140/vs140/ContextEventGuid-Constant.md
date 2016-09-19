---
title: "ContextEventGuid Constant"
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
ms.assetid: c3aec997-4941-433a-bdb6-f7ef6e5219fe
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ContextEventGuid Constant
A category GUID describing ETW events fired by the Concurrency Runtime that are directly related to contexts.  
  
## Syntax  
  
```  
const __declspec(selectany) GUID ContextEventGuid = { 0x5727A00F, 0x50BE, 0x4519, { 0x82, 0x56, 0xF7, 0x69, 0x98, 0x71, 0xFE, 0xCB } };  
```  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Context Class](../vs140/Context-Class.md)