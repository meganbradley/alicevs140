---
title: "reader_writer_lock::~reader_writer_lock Destructor"
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
ms.assetid: 2470306d-679d-4ba1-adcd-568745caa36a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reader_writer_lock::~reader_writer_lock Destructor
Destroys the `reader_writer_lock` object.  
  
## Syntax  
  
```  
~reader_writer_lock();  
```  
  
## Remarks  
 It is expected that the lock is no longer held when the destructor runs. Allowing the reader writer lock to destruct with the lock still held results in undefined behavior.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [reader_writer_lock Class](../vs140/reader_writer_lock-Class.md)