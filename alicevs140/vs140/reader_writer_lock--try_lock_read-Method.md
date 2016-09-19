---
title: "reader_writer_lock::try_lock_read Method"
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
ms.assetid: 558021f3-d86b-4cd7-91be-e3fed8a69ef9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reader_writer_lock::try_lock_read Method
Attempts to acquire the reader-writer lock as a reader without blocking.  
  
## Syntax  
  
```  
bool try_lock_read();  
```  
  
## Return Value  
 If the lock was acquired, the value `true`; otherwise, the value `false`.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [reader_writer_lock Class](../vs140/reader_writer_lock-Class.md)   
 [reader_writer_lock::unlock Method](../vs140/reader_writer_lock--unlock-Method.md)