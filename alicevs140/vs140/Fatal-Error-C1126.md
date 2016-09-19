---
title: "Fatal Error C1126"
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
ms.assetid: f22b26a6-8ad7-47cf-a237-196c8ea60aca
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1126
'identifier' : automatic allocation exceeds size  
  
 Space allocated for local variables of a function (plus a limited amount of space used by the compiler, such as an extra 20 bytes for swappable functions) exceeds the limit.  
  
 To correct this error, use `malloc` or `new` to allocate large amounts of data.