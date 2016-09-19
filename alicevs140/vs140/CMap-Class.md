---
title: "CMap Class"
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
ms.assetid: 640a45ab-0993-4def-97ec-42cc78eb10b9
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap Class
A dictionary collection class that maps unique keys to values.  
  
## Syntax  
  
```  
template< class KEY, class ARG_KEY, class VALUE, class ARG_VALUE >class CMap : public CObject  
```  
  
#### Parameters  
 `KEY`  
 Class of the object used as the key to the map.  
  
 `ARG` *_* `KEY`  
 Data type used for `KEY` arguments; usually a reference to `KEY`.  
  
 `VALUE`  
 Class of the object stored in the map.  
  
 `ARG` *_* `VALUE`  
 Data type used for `VALUE` arguments; usually a reference to `VALUE`.  
  
## Members  
  
### Public Structures  
  
|Name|Description|  
|----------|-----------------|  
|[CMap::CPair](#cmap__cpair)|A nested structure containing a key value and the value of the associated object.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMap::CMap](#cmap__cmap)|Constructs a collection that maps keys to values.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMap::GetCount](#cmap__getcount)|Returns the number of elements in this map.|  
|[CMap::GetHashTableSize](#cmap__gethashtablesize)|Returns the number of elements in the hash table.|  
|[CMap::GetNextAssoc](#cmap__getnextassoc)|Gets the next element for iterating.|  
|[CMap::GetSize](#cmap__getsize)|Returns the number of elements in this map.|  
|[CMap::GetStartPosition](#cmap__getstartposition)|Returns the position of the first element.|  
|[CMap::InitHashTable](#cmap__inithashtable)|Initializes the hash table and specifies its size.|  
|[CMap::IsEmpty](#cmap__isempty)|Tests for the empty-map condition (no elements).|  
|[CMap::Lookup](#cmap__lookup)|Looks up the value mapped to a given key.|  
|[CMap::PGetFirstAssoc](#cmap__pgetfirstassoc)|Returns a pointer to the first element.|  
|[CMap::PGetNextAssoc](#cmap__pgetnextassoc)|Gets a pointer to the next element for iterating.|  
|[CMap::PLookup](#cmap__plookup)|Returns a pointer to a key whose value matches the specified value.|  
|[CMap::RemoveAll](#cmap__removeall)|Removes all the elements from this map.|  
|[CMap::RemoveKey](#cmap__removekey)|Removes an element specified by a key.|  
|[CMap::SetAt](#cmap__setat)|Inserts an element into the map; replaces an existing element if a matching key is found.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CMap::operator &#91;&#93;](#cmap__operator_at)|Inserts an element into the map â€” operator substitution for `SetAt`.|  
  
## Remarks  
 Once you have inserted a key-value pair (element) into the map, you can efficiently retrieve or delete the pair using the key to access it. You can also iterate over all the elements in the map.  
  
 A variable of type **POSITION** is used for alternate access to entries. You can use a **POSITION** to "remember" an entry and to iterate through the map. You might think that this iteration is sequential by key value; it is not. The sequence of retrieved elements is indeterminate.  
  
 Certain member functions of this class call global helper functions that must be customized for most uses of the `CMap` class. See [Collection Class Helpers](../vs140/Collection-Class-Helpers.md) in the Macros and Globals section of the `MFC``Reference`.  
  
 `CMap` overrides [CObject::Serialize](../vs140/CObject-Class.md#cobject__serialize) to support serialization and dumping of its elements. If a map is stored to an archive using `Serialize`, each map element is serialized in turn. The default implementation of the `SerializeElements` helper function does a bitwise write. For information about serialization of pointer collection items derived from `CObject` or other user defined types, see [How to: Make a Type-Safe Collection](../vs140/How-to--Make-a-Type-Safe-Collection.md).  
  
 If you need a diagnostic dump of the individual elements in the map (the keys and values), you must set the depth of the dump context to 1 or greater.  
  
 When a `CMap` object is deleted, or when its elements are removed, the keys and values both are removed.  
  
 Map class derivation is similar to list derivation. See the article [Collections](../vs140/Collections.md) for an illustration of the derivation of a special-purpose list class.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 `CMap`  
  
## Requirements  
 **Header:** afxtempl.h  
  
##  <a name="cmap__cmap"></a>  CMap::CMap  
 Constructs an empty map.  
  
```  
CMap(    INT_PTR nBlockSize = 10 );  
  
```  
  
### Parameters  
 `nBlockSize`  
 Specifies the memory-allocation granularity for extending the map.  
  
### Remarks  
 As the map grows, memory is allocated in units of `nBlockSize` entries.  
  
### Example  
 [!CODE [NVC_MFCCollections#56](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#56)]  
  
##  <a name="cmap__cpair"></a>  CMap::CPair  
 Contains a key value and the value of the associated object.  
  
### Remarks  
 This is a nested structure within class [CMap](../vs140/CMap-Class.md).  
  
 The structure is composed of two fields:  
  
-   **keyÂ Â Â** The actual value of the key type.  
  
-   **valueÂ Â Â** The value of the associated object.  
  
 It is used to store the return values from [CMap::PLookup](#cmap__plookup), [CMap::PGetFirstAssoc](#cmap__pgetfirstassoc), and [CMap::PGetNextAssoc](#cmap__pgetnextassoc).  
  
### Example  
 For an example of usage, see the example for [CMap::PLookup](#cmap__plookup).  
  
##  <a name="cmap__getcount"></a>  CMap::GetCount  
 Retrieves the number of elements in the map.  
  
```  
INT_PTR GetCount( ) const;  
  
```  
  
### Return Value  
 The number of elements.  
  
### Example  
 See the example for [CMap::Lookup](#cmap__lookup).  
  
##  <a name="cmap__gethashtablesize"></a>  CMap::GetHashTableSize  
 Determines the number of elements in the hash table for the map.  
  
```  
UINT GetHashTableSize( ) const;  
  
```  
  
### Return Value  
 The number of elements in the hash table.  
  
### Example  
 [!CODE [NVC_MFCCollections#57](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#57)]  
  
##  <a name="cmap__getnextassoc"></a>  CMap::GetNextAssoc  
 Retrieves the map element at `rNextPosition`, then updates `rNextPosition` to refer to the next element in the map.  
  
```  
void GetNextAssoc(    POSITION& rNextPosition , KEY & rKey , VALUE & rValue ) const;  
  
```  
  
### Parameters  
 `rNextPosition`  
 Specifies a reference to a **POSITION** value returned by a previous `GetNextAssoc` or `GetStartPosition` call.  
  
 *KEY*  
 Template parameter specifying the type of the map's key.  
  
 `rKey`  
 Specifies the returned key of the retrieved element.  
  
 *VALUE*  
 Template parameter specifying the type of the map's value.  
  
 `rValue`  
 Specifies the returned value of the retrieved element.  
  
### Remarks  
 This function is most useful for iterating through all the elements in the map. Note that the position sequence is not necessarily the same as the key value sequence.  
  
 If the retrieved element is the last in the map, then the new value of `rNextPosition` is set to **NULL**.  
  
### Example  
 See the example for [CMap::SetAt](#cmap__setat).  
  
##  <a name="cmap__getsize"></a>  CMap::GetSize  
 Returns the number of map elements.  
  
```  
INT_PTR GetSize( ) const;  
  
```  
  
### Return Value  
 The number of items in the map.  
  
### Remarks  
 Call this method to retrieve the number of elements in the map.  
  
### Example  
 [!CODE [NVC_MFCCollections#58](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#58)]  
  
##  <a name="cmap__getstartposition"></a>  CMap::GetStartPosition  
 Starts a map iteration by returning a **POSITION** value that can be passed to a `GetNextAssoc` call.  
  
```  
POSITION GetStartPosition( ) const;  
  
```  
  
### Return Value  
 A **POSITION** value that indicates a starting position for iterating the map; or **NULL** if the map is empty.  
  
### Remarks  
 The iteration sequence is not predictable; therefore, the "first element in the map" has no special significance.  
  
### Example  
 See the example for [CMap::SetAt](#cmap__setat).  
  
##  <a name="cmap__inithashtable"></a>  CMap::InitHashTable  
 Initializes the hash table.  
  
```  
void InitHashTable(    UINT hashSize, BOOL  bAllocNow  = TRUEÂ );  
  
```  
  
### Parameters  
 `hashSize`  
 Number of entries in the hash table.  
  
 `bAllocNow`  
 If **TRUE**, allocates the hash table upon initialization; otherwise the table is allocated when needed.  
  
### Remarks  
 For best performance, the hash table size should be a prime number. To minimize collisions, the size should be roughly 20 percent larger than the largest anticipated data set.  
  
### Example  
 See the example for [CMap::Lookup](#cmap__lookup).  
  
##  <a name="cmap__isempty"></a>  CMap::IsEmpty  
 Determines whether the map is empty.  
  
```  
BOOL IsEmpty( ) const;  
  
```  
  
### Return Value  
 Nonzero if this map contains no elements; otherwise 0.  
  
### Example  
 See the example for [CMap::RemoveAll](#cmap__removeall).  
  
##  <a name="cmap__lookup"></a>  CMap::Lookup  
 Looks up the value mapped to a given key.  
  
```  
BOOL Lookup( ARG_KEY key , VALUE & rValue ) const;  
  
```  
  
### Parameters  
 `ARG_KEY`  
 Template parameter specifying the type of the `key` value.  
  
 `key`  
 Specifies the key that identifies the element to be looked up.  
  
 *VALUE*  
 Specifies the type of the value to be looked up.  
  
 `rValue`  
 Receives the looked-up value.  
  
### Return Value  
 Nonzero if the element was found; otherwise 0.  
  
### Remarks  
 `Lookup` uses a hashing algorithm to quickly find the map element with a key that exactly matches the given key.  
  
### Example  
 [!CODE [NVC_MFCCollections#58](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#58)]  
  
##  <a name="cmap__operator_at"></a>  CMap::operator [ ]  
 A convenient substitute for the `SetAt` member function.  
  
```  
VALUE & operator[](ARG_KEY key);  
  
```  
  
### Parameters  
 *VALUE*  
 Template parameter specifying the type of the map value.  
  
 `ARG_KEY`  
 Template parameter specifying the type of the key value.  
  
 `key`  
 The key used to retrieve the value from the map.  
  
### Remarks  
 Thus it can be used only on the left side of an assignment statement (an l-value). If there is no map element with the specified key, then a new element is created.  
  
 There is no "right side" (r-value) equivalent to this operator because there is a possibility that a key may not be found in the map. Use the `Lookup` member function for element retrieval.  
  
### Example  
 See the example for [CMap::Lookup](#cmap__lookup).  
  
##  <a name="cmap__pgetfirstassoc"></a>  CMap::PGetFirstAssoc  
 Returns the first entry of the map object.  
  
```  
const CPair* PGetFirstAssoc( ) const;Â CPair* PGetFirstAssoc( );  
  
```  
  
### Return Value  
 A pointer to the first entry in the map; see [CMap::CPair](#cmap__cpair). If the map contains no entries, the value is **NULL**.  
  
### Remarks  
 Call this function to return a pointer the first element in the map object.  
  
### Example  
 [!CODE [NVC_MFCCollections#59](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#59)]  
  
##  <a name="cmap__pgetnextassoc"></a>  CMap::PGetNextAssoc  
 Retrieves the map element pointed to by `pAssocRec`.  
  
```  
const CPair *PGetNextAssoc(    const CPair*  pAssocRet ) const; CPair *PGetNextAssoc(    const CPair*  pAssocRet );  
  
```  
  
### Parameters  
 *pAssocRet*  
 Points to a map entry returned by a previous [PGetNextAssoc](#vclrfcmappgetnextassoc) or [PGetFirstAssoc](#cmap__pgetfirstassoc) call.  
  
### Return Value  
 A pointer to the next entry in the map; see [CMap::CPair](#cmap__cpair). If the element is the last in the map, the value is **NULL**.  
  
### Remarks  
 Call this method to iterate through all the elements in the map. Retrieve the first element with a call to `PGetFirstAssoc` and then iterate through the map with successive calls to `PGetNextAssoc`.  
  
### Example  
 See the example for [CMap::PGetFirstAssoc](#cmap__pgetfirstassoc).  
  
##  <a name="cmap__plookup"></a>  CMap::PLookup  
 Finds the value mapped to a given key.  
  
```  
const CPair* PLookup(    ARG_KEY  key ) const; CPair* PLookup(Â    ARG_KEY  keyÂ );  
  
```  
  
### Parameters  
 `key`  
 Key for the element to be searched for.  
  
### Return Value  
 A pointer to a key structure; see [CMap::CPair](#cmap__cpair). If no match is found, `CMap::PLookup` returns `NULL`.  
  
### Remarks  
 Call this method to search for a map element with a key that exactly matches the given key.  
  
### Example  
 [!CODE [NVC_MFCCollections#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#60)]  
  
##  <a name="cmap__removeall"></a>  CMap::RemoveAll  
 Removes all the values from this map by calling the global helper function **DestructElements**.  
  
```  
void RemoveAll( );  
  
```  
  
### Remarks  
 The function works correctly if the map is already empty.  
  
### Example  
 [!CODE [NVC_MFCCollections#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#61)]  
  
##  <a name="cmap__removekey"></a>  CMap::RemoveKey  
 Looks up the map entry corresponding to the supplied key; then, if the key is found, removes the entry.  
  
```  
BOOL RemoveKey( ARG_KEY key );  
  
```  
  
### Parameters  
 `ARG_KEY`  
 Template parameter specifying the type of the key.  
  
 `key`  
 Key for the element to be removed.  
  
### Return Value  
 Nonzero if the entry was found and successfully removed; otherwise 0.  
  
### Remarks  
 The **DestructElements** helper function is used to remove the entry.  
  
### Example  
 See the example for [CMap::SetAt](#cmap__setat).  
  
##  <a name="cmap__setat"></a>  CMap::SetAt  
 The primary means to insert an element in a map.  
  
```  
void SetAt( ARG_KEY key , ARG_VALUE newValue );  
  
```  
  
### Parameters  
 `ARG_KEY`  
 Template parameter specifying the type of the `key` parameter.  
  
 `key`  
 Specifies the key of the new element.  
  
 `ARG_VALUE`  
 Template parameter specifying the type of the `newValue` parameter.  
  
 `newValue`  
 Specifies the value of the new element.  
  
### Remarks  
 First, the key is looked up. If the key is found, then the corresponding value is changed; otherwise a new key-value pair is created.  
  
### Example  
 [!CODE [NVC_MFCCollections#62](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#62)]  
  
## See Also  
 [MFC Sample COLLECT](../vs140/Visual-C---Samples.md)   
 [Base Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)