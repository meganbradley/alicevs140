---
title: "CComPtr Class"
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
ms.assetid: 22d9ea8d-ed66-4c34-940f-141db11e83bd
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtr Class
A smart pointer class for managing COM interface pointers.  
  
## Syntax  
  
```  
  
template<  
      class  T >  
   class CComPtr  
  
```  
  
#### Parameters  
 `T`  
 A COM interface specifying the type of pointer to be stored.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComPtr::CComPtr](../vs140/CComPtr--CComPtr.md)|The constructor.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CComPtr::operator =](../vs140/CComPtr--operator-=.md)|Assigns a pointer to the member pointer.|  
  
## Remarks  
 ATL uses `CComPtr` and [CComQIPtr](../vs140/CComQIPtr-Class.md) to manage COM interface pointers. Both are derived from [CComPtrBase](../vs140/CComPtrBase-Class.md), and both perform automatic reference counting.  
  
 The **CComPtr** and [CComQIPtr](../vs140/CComQIPtr-Class.md) classes can help eliminate memory leaks by performing automatic reference counting.  The following functions both perform the same logical operations; however, note how the second version may be less error-prone by using the **CComPtr** class:  
  
 [!CODE [NVC_ATL_Utilities#130](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#130)]  
  
 [!CODE [NVC_ATL_Utilities#131](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#131)]  
  
 In Debug builds, link atlsd.lib for code tracing.  
  
## Inheritance Hierarchy  
 [CComPtrBase](../vs140/CComPtrBase-Class.md)  
  
 `CComPtr`  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="ccomptr__ccomptr"></a>  CComPtr::CComPtr  
 The constructor.  
  
```  
  
CComPtr( ) throw ( );   
   CComPtr(  
      T*  lp  
   ) throw ( );  
   CComPtr (  
      const CComPtr<  T  
    >&  lp  
   ) throw ( );  
  
```  
  
### Parameters  
 `lp`  
 Used to initialize the interface pointer.  
  
 `T`  
 A COM interface.  
  
##  <a name="ccomptr__operator__eq"></a>  CComPtr::operator =  
 Assignment operator.  
  
```  
T  
  * operator =( T  
  *  lp  
  ) throw ( );  T  
  * operator =(  
     const CComPtr<  T  
   >&  lp  
  ) throw ( );  
  
```  
  
### Return Value  
 Returns a pointer to the updated `CComPtr` object  
  
### Remarks  
 This operation AddRefs the new object and releases the existing object, if one exists.  
  
## See Also  
 [CComPtr::CComPtr](../vs140/CComPtr--CComPtr.md)   
 [CComQIPtr::CComQIPtr](../vs140/CComQIPtr--CComQIPtr.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)