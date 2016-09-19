---
title: "CSimpleStringT::ReleaseBufferSetLength"
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
ms.assetid: 457d7c1c-0d0d-4dd7-9f25-c25735d60cfe
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::ReleaseBufferSetLength
Releases control of the buffer allocated by [GetBuffer](../vs140/CSimpleStringT--GetBuffer.md).  
  
## Syntax  
  
```  
  
      void ReleaseBufferSetLength(  
   int nNewLength   
);  
```  
  
#### Parameters  
 `nNewLength`  
 The length of the string being released  
  
## Remarks  
 This function is functionally similar to [ReleaseBuffer](../vs140/CSimpleStringT--ReleaseBuffer.md) except that a valid length for the string object must be passed.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)