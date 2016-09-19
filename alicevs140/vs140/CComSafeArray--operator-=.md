---
title: "CComSafeArray::operator ="
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
ms.assetid: 9246e4a2-0538-4d56-8054-fb97d310f52d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      ATL::CComSafeArray< T > & operator =(  
   const ATL::CComSafeArray & saSrc   
);  
ATL::CComSafeArray< T > & operator =(  
   const SAFEARRAY * psaSrc   
);  
```  
  
#### Parameters  
 `saSrc`  
 A reference to a `CComSafeArray` object.  
  
 `psaSrc`  
 A pointer to a **SAFEARRAY** object.  
  
## Return Value  
 Returns the type of data stored in the array.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)