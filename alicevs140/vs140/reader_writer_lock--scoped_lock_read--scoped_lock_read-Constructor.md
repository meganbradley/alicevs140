---
title: "reader_writer_lock::scoped_lock_read::scoped_lock_read Constructor"
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
ms.assetid: b01a1548-4ecb-48e6-b80d-1befd7eff261
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reader_writer_lock::scoped_lock_read::scoped_lock_read Constructor
Constructs a `scoped_lock_read` object and acquires the `reader_writer_lock` object passed in the `_Reader_writer_lock` parameter as a reader. If the lock is held by another thread as a writer or there are pending writers, this call will block.  
  
## Syntax  
  
```  
explicit _CRTIMP scoped_lock_read(  
   reader_writer_lock& _Reader_writer_lock  
);  
```  
  
#### Parameters  
 `_Reader_writer_lock`  
 The `reader_writer_lock` object to acquire as a reader.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [reader_writer_lock::scoped_lock_read Class](../vs140/reader_writer_lock--scoped_lock_read-Class.md)