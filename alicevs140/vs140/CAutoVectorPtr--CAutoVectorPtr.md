---
title: "CAutoVectorPtr::CAutoVectorPtr"
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
ms.assetid: b4154dc2-900b-4630-8fba-b02784fa8ab5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtr::CAutoVectorPtr
The constructor.  
  
## Syntax  
  
```  
  
      CAutoVectorPtr( ) throw( );   
explicit CAutoVectorPtr(  
   T* p   
) throw( );  
CAutoVectorPtr(  
   CAutoVectorPtr< T >& p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 An existing pointer.  
  
## Remarks  
 The `CAutoVectorPtr` object can be created using an existing pointer, in which case it transfers ownership of the pointer.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)   
 [CAutoVectorPtr::~CAutoVectorPtr](../vs140/CAutoVectorPtr--~CAutoVectorPtr.md)