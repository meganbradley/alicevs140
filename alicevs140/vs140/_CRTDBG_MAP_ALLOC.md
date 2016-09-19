---
title: "_CRTDBG_MAP_ALLOC"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 435242b8-caea-4063-b765-4a608200312b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CRTDBG_MAP_ALLOC
When the **_CRTDBG_MAP_ALLOC** flag is defined in the debug version of an application, the base version of the heap functions are directly mapped to their debug versions. The flag is used in Crtdbg.h to do the mapping. This flag is only available when the [_DEBUG](../vs140/_DEBUG.md) flag has been defined in the application.  
  
 For more information about using the debug version versus the base version of a heap function, see [Using the Debug Version Versus the Base Version](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md).  
  
## See Also  
 [Control Flags](../vs140/Control-Flags.md)