---
title: "Expression Evaluator Error CXX0019"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 4c6431fd-3310-4a61-934d-58b070b330fe
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Evaluator Error CXX0019
bad type cast  
  
 The C expression evaluator cannot perform the type cast as written.  
  
 This error is identical to CAN0019.  
  
### To fix by checking the following possible causes  
  
1.  The specified type is unknown.  
  
2.  There were too many levels of pointer types. For example, the type cast  
  
    ```  
    (char **)h_message  
    ```  
  
     cannot be evaluated by the C expression evaluator.