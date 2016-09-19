---
title: "CComPtrBase::operator =="
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
ms.assetid: ca2235b3-9812-47f5-bd20-ab1e19d39d8c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::operator ==
The equality operator.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   T * pT   
) const throw( );  
```  
  
#### Parameters  
 *pT*  
 A pointer to an object.  
  
## Return Value  
 Returns true if `CComPtrBase` and *pT* point to the same object, false otherwise.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)