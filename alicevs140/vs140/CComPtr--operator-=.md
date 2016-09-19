---
title: "CComPtr::operator ="
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
ms.assetid: b84136f8-4881-4434-98f1-10f5a2bb5f5d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtr::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      T  
      * operator =(  
   T* lp   
) throw ( );   
T* operator =(  
   const CComPtr< T >& lp   
) throw ( );  
```  
  
## Return Value  
 Returns a pointer to the updated `CComPtr` object  
  
## Remarks  
 This operation AddRefs the new object and releases the existing object, if one exists.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtr Class](../vs140/CComPtr-Class.md)   
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)