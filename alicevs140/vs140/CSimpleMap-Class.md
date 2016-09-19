---
title: "CSimpleMap Class"
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
ms.assetid: 61b06eb4-ae73-44b0-a305-0afb5a33e8b1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap Class
This class provides support for a simple mapping array.  
  
## Syntax  
  
```  
  
template <   
      class  TKey,  
      class  TVal,  
      class  TEqual  
    = CSimpleMapEqualHelper<  TKey  
   ,  TVal  
    >   
   >   
   class CSimpleMap  
  
```  
  
#### Parameters  
 `TKey`  
 The key element type.  
  
 `TVal`  
 The value element type.  
  
 `TEqual`  
 A trait object, defining the equality test for elements of type `T`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleMap::_ArrayElementType](../vs140/CSimpleMap--_ArrayElementType.md)|Typedef for the value type.|  
|[CSimpleMap::_ArrayKeyType](../vs140/CSimpleMap--_ArrayKeyType.md)|Typedef for the key type.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleMap::CSimpleMap](../vs140/CSimpleMap--CSimpleMap.md)|The constructor.|  
|[CSimpleMap::~CSimpleMap](../vs140/CSimpleMap--~CSimpleMap.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleMap::Add](../vs140/CSimpleMap--Add.md)|Adds a key and associated value to the map array.|  
|[CSimpleMap::FindKey](../vs140/CSimpleMap--FindKey.md)|Finds a specific key.|  
|[CSimpleMap::FindVal](../vs140/CSimpleMap--FindVal.md)|Finds a specific value.|  
|[CSimpleMap::GetKeyAt](../vs140/CSimpleMap--GetKeyAt.md)|Retrieves the specified key.|  
|[CSimpleMap::GetSize](../vs140/CSimpleMap--GetSize.md)|Returns the number of entries in the mapping array.|  
|[CSimpleMap::GetValueAt](../vs140/CSimpleMap--GetValueAt.md)|Retrieves the specified value.|  
|[CSimpleMap::Lookup](../vs140/CSimpleMap--Lookup.md)|Returns the value associated with the given key.|  
|[CSimpleMap::Remove](../vs140/CSimpleMap--Remove.md)|Removes a key and matching value.|  
|[CSimpleMap::RemoveAll](../vs140/CSimpleMap--RemoveAll.md)|Removes all keys and values.|  
|[CSimpleMap::RemoveAt](../vs140/CSimpleMap--RemoveAt.md)|Removes a specific key and matching value.|  
|[CSimpleMap::ReverseLookup](../vs140/CSimpleMap--ReverseLookup.md)|Returns the key associated with the given value.|  
|[CSimpleMap::SetAt](../vs140/CSimpleMap--SetAt.md)|Sets the value associated with the given key.|  
|[CSimpleMap::SetAtIndex](../vs140/CSimpleMap--SetAtIndex.md)|Sets the specific key and value.|  
  
## Remarks  
 `CSimpleMap` provides support for a simple mapping array of any given type `T`, managing an unordered array of key elements and their associated values.  
  
 The parameter `TEqual` provides a means of defining an equality function for two elements of type `T`. By creating a class similar to [CSimpleMapEqualHelper](../vs140/CSimpleMapEqualHelper-Class.md), it is possible to alter the behavior of the equality test for any given array. For example, when dealing with an array of pointers, it may be useful to define the equality as depending on the values the pointers reference. The default implementation utilizes **operator==()**.  
  
 Both `CSimpleMap` and [CSimpleArray](../vs140/CSimpleArray-Class.md) are provided for compatibility with previous ATL releases, and more complete and efficient collection implementations are provided by [CAtlArray](../vs140/CAtlArray-Class.md) and [CAtlMap](../vs140/CAtlMap-Class.md).  
  
 Unlike other map collections in ATL and MFC, this class is implemented with a simple array, and lookup searches require a linear search. `CAtlMap` should be used when the array contains a large number of elements.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## Example  
 [!CODE [NVC_ATL_Utilities#91](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#91)]  
  
##  <a name="csimplemap__add"></a>  CSimpleMap::Add  
 Adds a key and associated value to the map array.  
  
```  
  
BOOL Add(  
      const TKey&  key,  
      const TVal&  val  
   );  
  
```  
  
### Parameters  
 `key`  
 The key.  
  
 *val*  
 The associated value.  
  
### Return Value  
 Returns TRUE if the key and value were successfully added, FALSE otherwise.  
  
### Remarks  
 Each key and value pair added causes the mapping array memory to be freed and reallocated, in order to ensure the data for each is always stored contiguously. That is, the second key element always directly follows the first key element in memory and so on.  
  
##  <a name="csimplemap___arrayelementtype"></a>  CSimpleMap::_ArrayElementType  
 A typedef for the key type.  
  
```  
  
typedef TVal _ArrayElementType;  
  
```  
  
##  <a name="csimplemap___arraykeytype"></a>  CSimpleMap::_ArrayKeyType  
 A typedef for the value type.  
  
```  
  
typedef TKey _ArrayKeyType;  
  
```  
  
##  <a name="csimplemap__csimplemap"></a>  CSimpleMap::CSimpleMap  
 The constructor.  
  
```  
  
CSimpleMap( );  
  
```  
  
### Remarks  
 Initializes the data members.  
  
##  <a name="csimplemap___dtorcsimplemap"></a>  CSimpleMap::~CSimpleMap  
 The destructor.  
  
```  
  
~CSimpleMap( );  
  
```  
  
### Remarks  
 Frees all allocated resources.  
  
##  <a name="csimplemap__findkey"></a>  CSimpleMap::FindKey  
 Finds a specific key.  
  
```  
  
int FindKey(  
      const TKey&  key  
   ) const;  
  
```  
  
### Parameters  
 `key`  
 The key to search for.  
  
### Return Value  
 Returns the index of the key if found, otherwise returns -1.  
  
##  <a name="csimplemap__findval"></a>  CSimpleMap::FindVal  
 Finds a specific value.  
  
```  
  
int FindVal(  
      const TVal&  val  
   ) const;  
  
```  
  
### Parameters  
 *val*  
 The value for which to search.  
  
### Return Value  
 Returns the index of the value if it is found, otherwise returns -1.  
  
##  <a name="csimplemap__getkeyat"></a>  CSimpleMap::GetKeyAt  
 Retrieves the key at the specified index.  
  
```  
  
TKey& GetKeyAt(  
      int  nIndex  
   ) const;  
  
```  
  
### Parameters  
 `nIndex`  
 The index of the key to return.  
  
### Return Value  
 Returns the key referenced by `nIndex`.  
  
### Remarks  
 The index passed by `nIndex` must be valid for the return value to be meaningful.  
  
##  <a name="csimplemap__getsize"></a>  CSimpleMap::GetSize  
 Returns the number of entries in the mapping array.  
  
```  
  
int GetSize( ) const;  
  
```  
  
### Return Value  
 Returns the number of entries (a key and value is one entry) in the mapping array.  
  
##  <a name="csimplemap__getvalueat"></a>  CSimpleMap::GetValueAt  
 Retrieves the value at the specific index.  
  
```  
  
TVal& GetValueAt(  
      int  nIndex  
   ) const;  
  
```  
  
### Parameters  
 `nIndex`  
 The index of the value to return.  
  
### Return Value  
 Returns the value referenced by `nIndex`.  
  
### Remarks  
 The index passed by `nIndex` must be valid for the return value to be meaningful.  
  
##  <a name="csimplemap__lookup"></a>  CSimpleMap::Lookup  
 Returns the value associated with the given key.  
  
```  
  
TVal Lookup(  
      const TKey&  key  
   ) const;  
  
```  
  
### Parameters  
 `key`  
 The key.  
  
### Return Value  
 Returns the associated value. If no matching key is found, NULL is returned.  
  
##  <a name="csimplemap__remove"></a>  CSimpleMap::Remove  
 Removes a key and matching value.  
  
```  
  
BOOL Remove(  
      const TKey&  key  
   );  
  
```  
  
### Parameters  
 `key`  
 The key.  
  
### Return Value  
 Returns TRUE if the key, and matching value, were successfully removed, FALSE otherwise.  
  
##  <a name="csimplemap__removeall"></a>  CSimpleMap::RemoveAll  
 Removes all keys and values.  
  
```  
  
void RemoveAll( );  
  
```  
  
### Remarks  
 Removes all keys and values from the mapping array object.  
  
##  <a name="csimplemap__removeat"></a>  CSimpleMap::RemoveAt  
 Removes a key and associated value at the specified index.  
  
```  
  
BOOL RemoveAt(  
      int  nIndex  
   );  
  
```  
  
### Parameters  
 `nIndex`  
 The index of the key and associated value to remove.  
  
### Return Value  
 Returns TRUE on success, FALSE if the index specified is an invalid index.  
  
##  <a name="csimplemap__reverselookup"></a>  CSimpleMap::ReverseLookup  
 Returns the key associated with the given value.  
  
```  
  
TKey ReverseLookup(  
      const TVal&  val  
   ) const;  
  
```  
  
### Parameters  
 *val*  
 The value.  
  
### Return Value  
 Returns the associated key. If no matching key is found, NULL is returned.  
  
##  <a name="csimplemap__setat"></a>  CSimpleMap::SetAt  
 Sets the value associated with the given key.  
  
```  
  
BOOL SetAt(  
      const TKey&  key,  
      const TVal&  val  
   );  
  
```  
  
### Parameters  
 `key`  
 The key.  
  
 *val*  
 The new value to assign.  
  
### Return Value  
 Returns TRUE if the key was found, and the value was successfully changed, FALSE otherwise.  
  
##  <a name="csimplemap__setatindex"></a>  CSimpleMap::SetAtIndex  
 Sets the key and value at a specified index.  
  
```  
  
BOOL SetAtIndex(  
      int  nIndex,  
      const TKey&  key,  
      const TVal&  val  
   );  
  
```  
  
### Parameters  
 `nIndex`  
 The index, referencing the key and value pairing to change.  
  
 `key`  
 The new key.  
  
 *val*  
 The new value.  
  
### Return Value  
 Returns TRUE if successful, FALSE if the index was not valid.  
  
### Remarks  
 Updates both the key and value pointed to by `nIndex`.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)