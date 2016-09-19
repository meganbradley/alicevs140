---
title: "CInterfaceList Class"
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
ms.assetid: 2077764d-25e5-4b3d-96c8-08a287bbcd25
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInterfaceList Class
This class provides methods useful when constructing a list of COM interface pointers.  
  
## Syntax  
  
```  
  
template<  
      class  I,  
      const IID*  piid  
    = & __uuidof(  I  
    )  
   >   
   class CInterfaceList : public CAtlList<  
      ATL::CComQIPtr<  I  
   ,  piid  
    >,  
      CComQIPtrElementTraits<  I  
   ,  piid  
    >>  
  
```  
  
#### Parameters  
 `I`  
 A COM interface specifying the type of pointer to be stored.  
  
 `piid`  
 A pointer to the IID of `I`.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CInterfaceList::CInterfaceList](../vs140/CInterfaceList--CInterfaceList.md)|The constructor for the interface list.|  
  
## Remarks  
 This class provides a constructor and derived methods for creating a list of COM interface pointers. Use [CInterfaceArray](../vs140/CInterfaceArray-Class.md) when an array is required.  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CAtlList](../vs140/CAtlList-Class.md)  
  
 `CInterfaceList`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cinterfacelist__cinterfacelist"></a>  CInterfaceList::CInterfaceList  
 The constructor for the interface list.  
  
```  
  
CInterfaceList(  
      UINT  nBlockSize  
    = 10   
   ) throw( );  
  
```  
  
### Parameters  
 `nBlockSize`  
 The block size, with a default of 10.  
  
### Remarks  
 The block size is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources.  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CComQIPtr Class](../vs140/CComQIPtr-Class.md)   
 [CComQIPtrElementTraits Class](../vs140/CComQIPtrElementTraits-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)