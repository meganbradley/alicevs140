---
title: "CAutoVectorPtr::operator ="
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
ms.assetid: 903c2d91-3663-4813-a49e-47c55124945d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtr::operator =
The assignment operator.  
  
## Syntax  
  
```  
  
      CAutoVectorPtr< T >& operator =(  
   CAutoVectorPtr< T >& p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 A pointer.  
  
## Return Value  
 Returns a reference to a **CAutoVectorPtr< T >**.  
  
## Remarks  
 The assignment operator detaches the `CAutoVectorPtr` object from any current pointer and attaches the new pointer, `p`, in its place.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)   
 [CAutoVectorPtr::Attach](../vs140/CAutoVectorPtr--Attach.md)   
 [CAutoVectorPtr::Detach](../vs140/CAutoVectorPtr--Detach.md)