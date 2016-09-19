---
title: "CHeapPtrList::CHeapPtrList"
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
ms.assetid: 85e1e526-0316-4d4b-a103-a344876d66ea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrList::CHeapPtrList
The constructor.  
  
## Syntax  
  
```  
  
      CHeapPtrList(  
   UINT nBlockSize = 10   
) throw( );  
```  
  
#### Parameters  
 `nBlockSize`  
 The block size.  
  
## Remarks  
 The block size is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrList Class](../vs140/CHeapPtrList-Class.md)