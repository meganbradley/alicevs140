---
title: "Heap Constants"
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
ms.assetid: 3f751bb9-2dc4-486f-b5f5-9061c96d3754
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Heap Constants
## Syntax  
  
```  
  
#include <malloc.h>  
  
```  
  
## Remarks  
 These constants give the return value indicating status of the heap.  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_HEAPBADBEGIN`|Initial header information was not found or was invalid.|  
|`_HEAPBADNODE`|Bad node was found, or heap is damaged.|  
|`_HEAPBADPTR`|**_pentry** field of **_HEAPINFO** structure does not contain valid pointer into heap (`_heapwalk` routine only).|  
|`_HEAPEMPTY`|Heap has not been initialized.|  
|`_HEAPEND`|End of heap was reached successfully (`_heapwalk` routine only).|  
|`_HEAPOK`|Heap is consistent (`_heapset` and `_heapchk` routines only). No errors so far; **_HEAPINFO** structure contains information about next entry (`_heapwalk` routine only).|  
  
## See Also  
 [_heapchk](../vs140/_heapchk.md)   
 [_heapset](../vs140/_heapset.md)   
 [_heapwalk](../vs140/_heapwalk.md)   
 [Global Constants](../vs140/Global-Constants.md)