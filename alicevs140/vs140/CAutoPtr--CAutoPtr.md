---
title: "CAutoPtr::CAutoPtr"
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
ms.assetid: 8e2131e1-c73f-419e-a200-eaaadb5e006f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::CAutoPtr
The constructor.  
  
## Syntax  
  
```  
  
      CAutoPtr( ) throw( );   
explicit CAutoPtr(  
   T* p   
) throw( );  
template< typename TSrc > CAutoPtr(  
   CAutoPtr< TSrc >& p   
) throw( );  
template< > CAutoPtr(  
   CAutoPtr< T >& p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 An existing pointer.  
  
 `TSrc`  
 The type being managed by another `CAutoPtr`, used to initialize the current object.  
  
## Remarks  
 The `CAutoPtr` object can be created using an existing pointer, in which case it transfers ownership of the pointer.  
  
## Example  
 See the example in the [CAutoPtr Overview](../vs140/CAutoPtr-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)   
 [CAutoPtr::~CAutoPtr](../vs140/CAutoPtr--~CAutoPtr.md)