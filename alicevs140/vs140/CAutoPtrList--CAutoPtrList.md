---
title: "CAutoPtrList::CAutoPtrList"
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
ms.assetid: 20a0af6a-58e4-4787-84bf-1015460daa84
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtrList::CAutoPtrList
The constructor.  
  
## Syntax  
  
```  
  
      CAutoPtrList(  
   UINT nBlockSize = 10   
) throw( );  
```  
  
#### Parameters  
 `nBlockSize`  
 The block size, with a default of 10.  
  
## Remarks  
 The block size is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAutoPtrList Class](../vs140/CAutoPtrList-Class.md)