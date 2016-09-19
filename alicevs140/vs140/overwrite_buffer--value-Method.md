---
title: "overwrite_buffer::value Method"
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
ms.assetid: 2a79b222-65e5-40ce-8ded-85e25ab07f22
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# overwrite_buffer::value Method
Gets a reference to the current payload of the message being stored in the `overwrite_buffer` messaging block.  
  
## Syntax  
  
```  
_Type value();  
```  
  
## Return Value  
 The payload of the currently stored message.  
  
## Remarks  
 The value stored in the `overwrite_buffer` could change immediately after this method returns. This method will wait until a message arrives if no message is currently stored in the `overwrite_buffer`.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [overwrite_buffer Class](../vs140/overwrite_buffer-Class.md)