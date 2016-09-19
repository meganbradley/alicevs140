---
title: "unsupported_feature::unsupported_feature Constructor"
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
ms.assetid: c105205e-0712-4a75-89c4-6960812c5a64
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unsupported_feature::unsupported_feature Constructor
Constructs a new instance of the unsupported_feature exception.  
  
## Syntax  
  
```  
explicit unsupported_feature(  
   const char * _Message  
) throw();  
  
unsupported_feature() throw();  
```  
  
#### Parameters  
 `_Message`  
 A description of the error.  
  
## Return Value  
 The `unsupported_feature` object.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [unsupported_feature Class](../vs140/unsupported_feature-Class.md)