---
title: "CRBMultiMap Class"
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
ms.assetid: 94d3ec0c-3e30-4ab7-a101-d8da4fb8add3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMultiMap Class
This class represents a mapping structure that allows each key can be associated with more than one value, using a Red-Black binary tree.  
  
## Syntax  
  
```  
  
template<  
      typename  K,  
      typename  V,  
      class  KTraits  
    = CElementTraits<  K  
    >,  
      class  VTraits  
    = CElementTraits<  V  
    >  
   > class CRBMultiMap : public CRBTree<  K  
   ,  V  
   ,  KTraits  
   ,  VTraits  
    >  
  
```  
  
#### Parameters  
 `K`  
 The key element type.  
  
 *V*  
 The value element type.  
  
 `KTraits`  
 The code used to copy or move key elements. See [CElementTraits Class](../vs140/CElementTraits-Class.md) for more details.  
  
 `VTraits`  
 The code used to copy or move value elements.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md)|The constructor.|  
|[CRBMultiMap::~CRBMultiMap](../vs140/CRBMultiMap--~CRBMultiMap.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md)|Call this method to find the position of the first element with a given key.|  
|[CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md)|Call this method to get the value associated with a given key, and update the position value.|  
|[CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md)|Call this method to get the element associated with a given key, and update the position value.|  
|[CRBMultiMap::Insert](../vs140/CRBMultiMap--Insert.md)|Call this method to insert an element pair into the map.|  
|[CRBMultiMap::RemoveKey](../vs140/CRBMultiMap--RemoveKey.md)|Call this method to remove all of the key/value elements for a given key.|  
  
## Remarks  
 `CRBMultiMap` provides support for a mapping array of any given type, managing an ordered array of key elements and values. Unlike the [CRBMap](../vs140/CRBMap-Class.md) class, each key can be associated with more than one value.  
  
 Elements (consisting of a key and a value) are stored in a binary tree structure, using the [CRBMultiMap::Insert](../vs140/CRBMultiMap--Insert.md) method. Elements can be removed using the [CRBMultiMap::RemoveKey](../vs140/CRBMultiMap--RemoveKey.md) method, which deletes all elements which match the given key.  
  
 Traversing the tree is made possible with methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md), [CRBTree::GetNext](../vs140/CRBTree--GetNext.md), and [CRBTree::GetNextValue](../vs140/CRBTree--GetNextValue.md). Accessing the potentially multiple values per key is possible using the [CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md), [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md), and [CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md) methods. See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md) for an illustration of this in practice.  
  
 The `KTraits` and `VTraits` parameters are traits classes that contain any supplemental code needed to copy or move elements.  
  
 `CRBMultiMap` is derived from [CRBTree](../vs140/CRBTree-Class.md), which implements a binary tree using the Red-Black algorithm. An alternative to `CRBMultiMap` and `CRBMap` is offered by the [CAtlMap](../vs140/CAtlMap-Class.md) class. When only a small number of elements needs to be stored, consider using the [CSimpleMap](../vs140/CSimpleMap-Class.md) class instead.  
  
 For a more complete discussion of the various collection classes and their features and performance characteristics, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CRBTree](../vs140/CRBTree-Class.md)  
  
 `CRBMultiMap`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="crbmultimap__crbmultimap"></a>  CRBMultiMap::CRBMultiMap  
 The constructor.  
  
```  
  
explicit CRBMultiMap(  
      size_t  nBlockSize  
    = 10   
   ) throw( );  
  
```  
  
### Parameters  
 `nBlockSize`  
 The block size.  
  
### Remarks  
 The `nBlockSize` parameter is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources. The default will allocate space for 10 elements at a time.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#85](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#85)]  
  
##  <a name="crbmultimap___dtorcrbmultimap"></a>  CRBMultiMap::~CRBMultiMap  
 The destructor.  
  
```  
  
~CRBMultiMap( ) throw( );  
  
```  
  
### Remarks  
 Frees any allocated resources.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
##  <a name="crbmultimap__findfirstwithkey"></a>  CRBMultiMap::FindFirstWithKey  
 Call this method to find the position of the first element with a given key.  
  
```  
  
POSITION FindFirstWithKey(  
      KINARGTYPE  key  
   ) const throw( );  
  
```  
  
### Parameters  
 `key`  
 Specifies the key that identifies the element to be found.  
  
### Return Value  
 Returns the POSITION of the first key/value element if the key is found, NULL otherwise.  
  
### Remarks  
 A key in the `CRBMultiMap` can have one or more associated values. This method will provide the position value of the first value (which may, in fact, be the only value) associated with that particular key. The position value returned can then be used with [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md) or [CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md) to obtain the value and update the position.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
### Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
##  <a name="crbmultimap__getnextvaluewithkey"></a>  CRBMultiMap::GetNextValueWithKey  
 Call this method to get the value associated with a given key and update the position value.  
  
```  
  
const V& GetNextValueWithKey(  
      POSITION&  pos,  
      KINARGTYPE  key  
   ) const throw( );  
   V& GetNextValueWithKey(  
      POSITION&  pos,  
      KINARGTYPE  key  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position value, obtained with either a call to [CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md) or [CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md), or a previous call to `GetNextValueWithKey`.  
  
 `key`  
 Specifies the key that identifies the element to be found.  
  
### Return Value  
 Returns the element pair associated with the given key.  
  
### Remarks  
 The position value is updated to point to the next value associated with the key. If no more values exist, the position value is set to NULL.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
### Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
##  <a name="crbmultimap__getnextwithkey"></a>  CRBMultiMap::GetNextWithKey  
 Call this method to get the element associated with a given key and update the position value.  
  
```  
  
const CPair* GetNextWithKey(  
      POSITION&  pos,  
      KINARGTYPE  key  
   ) const throw( );  
   CPair* GetNextWithKey(  
      POSITION&  pos,  
      KINARGTYPE  key  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position value, obtained with either a call to [CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md) or [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md), or a previous call to `GetNextWithKey`.  
  
 `key`  
 Specifies the key that identifies the element to be found.  
  
### Return Value  
 Returns the next [CRBTree::CPair Class](../vs140/CRBTree--CPair-Class.md) element associated with the given key.  
  
### Remarks  
 The position value is updated to point to the next value associated with the key. If no more values exist, the position value is set to NULL.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
##  <a name="crbmultimap__insert"></a>  CRBMultiMap::Insert  
 Call this method to insert an element pair into the map.  
  
```  
  
POSITION Insert(  
      KINARGTYPE  key,  
      VINARGTYPE  value  
   ) throw(...);  
  
```  
  
### Parameters  
 `key`  
 The key value to add to the `CRBMultiMap` object.  
  
 *value*  
 The value to add to the `CRBMultiMap` object, associated with `key`.  
  
### Return Value  
 Returns the position of the key/value element pair in the `CRBMultiMap` object.  
  
### Remarks  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
### Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
##  <a name="crbmultimap__removekey"></a>  CRBMultiMap::RemoveKey  
 Call this method to remove all of the key/value elements for a given key.  
  
```  
  
size_t RemoveKey(  
      KINARGTYPE  key  
   ) throw( );  
  
```  
  
### Parameters  
 `key`  
 Specifies the key that identifies the element(s) to be deleted.  
  
### Return Value  
 Returns the number of values associated with the given key.  
  
### Remarks  
 `RemoveKey` deletes all of the key/value elements that have a key that matches `key`.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
### Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)   
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CRBMap Class](../vs140/CRBMap-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)