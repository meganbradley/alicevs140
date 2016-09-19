---
title: "CAutoPtr::operator ="
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
ms.assetid: 8c17d902-8115-4e85-8b61-a4ee145f50e6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::operator =
The assignment operator.  
  
## Syntax  
  
```  
  
      template< >  
CAutoPtr< T > & operator =(  
   CAutoPtr< T > & p   
);  
template< typename TSrc >  
CAutoPtr< T > & operator =(  
   CAutoPtr< TSrc > & p   
);  
```  
  
#### Parameters  
 `p`  
 A pointer.  
  
 `TSrc`  
 A class type.  
  
## Return Value  
 Returns a reference to a **CAutoPtr< T >**.  
  
## Remarks  
 The assignment operator detaches the `CAutoPtr` object from any current pointer and attaches the new pointer, `p`, in its place.  
  
## Example  
 See the example in the [CAutoPtr Overview](../vs140/CAutoPtr-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)   
 [CAutoPtr::Attach](../vs140/CAutoPtr--Attach.md)   
 [CAutoPtr::Detach](../vs140/CAutoPtr--Detach.md)