---
title: "_ATL_MULTI_THREADED"
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
ms.topic: reference
ms.assetid: 23fb6460-e651-46e6-b207-8559ccf49608
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_MULTI_THREADED
A symbol that indicates the project will have objects that are marked as Both, Free or Neutral.  
  
## Syntax  
  
```  
  
_ATL_MULTI_THREADED  
  
```  
  
## Remarks  
 If this symbol is defined, ATL will pull in code that will correctly synchronize access to global data. New code should use the equivalent macro [_ATL_FREE_THREADED](../vs140/_ATL_FREE_THREADED.md) instead.  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)