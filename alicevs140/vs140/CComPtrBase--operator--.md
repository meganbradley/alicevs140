---
title: "CComPtrBase::operator &lt;"
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
ms.assetid: 3d06be72-f7cc-4127-a33f-2ac7cf6c1583
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::operator &lt;
The less-than operator.  
  
## Syntax  
  
```  
  
      bool operator <(  
   T * pT   
) const throw( );  
```  
  
#### Parameters  
 *pT*  
 A pointer to an object.  
  
## Return Value  
 Returns true if the pointer managed by current object is less than the pointer to which it is being compared.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)