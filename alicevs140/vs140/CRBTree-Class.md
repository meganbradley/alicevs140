---
title: "CRBTree Class"
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
ms.assetid: a1b1cb63-38e4-4fc2-bb28-f774d1721760
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree Class
This class provides methods for creating and utilizing a Red-Black tree.  
  
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
   > class CRBTree  
  
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
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CRBTree::KINARGTYPE](../vs140/CRBTree--KINARGTYPE.md)|Type used when a key is passed as an input argument.|  
|[CRBTree::KOUTARGTYPE](../vs140/CRBTree--KOUTARGTYPE.md)|Type used when a key is returned as an output argument.|  
|[CRBTree::VINARGTYPE](../vs140/CRBTree--VINARGTYPE.md)|Type used when a value is passed as an input argument.|  
|[CRBTree::VOUTARGTYPE](../vs140/CRBTree--VOUTARGTYPE.md)|Type used when a value is passed as an output argument.|  
  
### Public Classes  
  
|Name|Description|  
|----------|-----------------|  
|[CRBTree::CPair Class](../vs140/CRBTree--CPair-Class.md)|A class containing the key and value elements.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CRBTree::~CRBTree](../vs140/CRBTree--~CRBTree.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md)|Call this method to find the position of the element that uses the next available key.|  
|[CRBTree::GetAt](../vs140/CRBTree--GetAt.md)|Call this method to get the element at a given position in the tree.|  
|[CRBTree::GetCount](../vs140/CRBTree--GetCount.md)|Call this method to get the number of elements in the tree.|  
|[CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md)|Call this method to get the position value for the element at the head of the tree.|  
|[CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md)|Call this method to get the key from a given position in the tree.|  
|[CRBTree::GetNext](../vs140/CRBTree--GetNext.md)|Call this method to obtain a pointer to an element stored in the `CRBTree` object, and advance the position to the next element.|  
|[CRBTree::GetNextAssoc](../vs140/CRBTree--GetNextAssoc.md)|Call this method to get the key and value of an element stored in the map and advance the position to the next element.|  
|[CRBTree::GetNextKey](../vs140/CRBTree--GetNextKey.md)|Call this method to get the key of an element stored in the tree and advance the position to the next element.|  
|[CRBTree::GetNextValue](../vs140/CRBTree--GetNextValue.md)|Call this method to get the value of an element stored in the tree and advance the position to the next element.|  
|[CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md)|Call this method to obtain a pointer to an element stored in the `CRBTree` object, and then update the position to the previous element.|  
|[CRBTree::GetTailPosition](../vs140/CRBTree--GetTailPosition.md)|Call this method to get the position value for the element at the tail of the tree.|  
|[CRBTree::GetValueAt](../vs140/CRBTree--GetValueAt.md)|Call this method to retrieve the value stored at a given position in the `CRBTree` object.|  
|[CRBTree::IsEmpty](../vs140/CRBTree--IsEmpty.md)|Call this method to test for an empty tree object.|  
|[CRBTree::RemoveAll](../vs140/CRBTree--RemoveAll.md)|Call this method to remove all elements from the **CRBTree** object.|  
|[CRBTree::RemoveAt](../vs140/CRBTree--RemoveAt.md)|Call this method to remove the element at the given position in the **CRBTree** object.|  
|[CRBTree::SetValueAt](../vs140/CRBTree--SetValueAt.md)|Call this method to change the value stored at a given position in the `CRBTree` object.|  
  
## Remarks  
 A Red-Black tree is a binary search tree that uses an extra bit of information per node to ensure that it remains "balanced," that is, the tree height doesn't grow disproportionately large and affect performance.  
  
 This template class is designed to be used by [CRBMap](../vs140/CRBMap-Class.md) and [CRBMultiMap](../vs140/CRBMultiMap-Class.md). The bulk of the methods that make up these derived classes are provided by `CRBTree`.  
  
 For a more complete discussion of the various collection classes and their features and performance characteristics, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="crbtree__cpair_class"></a>  CRBTree::CPair Class  
 A class containing the key and value elements.  
  
```  
  
class CPair : public __POSITION  
  
```  
  
### Remarks  
 This class is used by the methods [CRBTree::GetAt](../vs140/CRBTree--GetAt.md), [CRBTree::GetNext](../vs140/CRBTree--GetNext.md), and [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md) to access the key and value elements stored in the tree structure.  
  
 The members are as follows:  
  
|||  
|-|-|  
|[m_key](../vs140/CAtlMap--CPair--m_key.md)|The data member storing the key element.|  
|[m_value](../vs140/CAtlMap--CPair--m_value.md)|The data member storing the value element.|  
  
##  <a name="crbtree___dtorcrbtree"></a>  CRBTree::~CRBTree  
 The destructor.  
  
```  
  
~CRBTree( ) throw( );  
  
```  
  
### Remarks  
 Frees any allocated resources. Calls [CRBTree::RemoveAll](../vs140/CRBTree--RemoveAll.md) to delete all elements.  
  
##  <a name="crbtree__findfirstkeyafter"></a>  CRBTree::FindFirstKeyAfter  
 Call this method to find the position of the element that uses the next available key.  
  
```  
  
POSITION FindFirstKeyAfter(  
      KINARGTYPE  key  
   ) const throw( );  
  
```  
  
### Parameters  
 `key`  
 A key value.  
  
### Return Value  
 Returns the position value of the element that uses the next available key. If there are no more elements, NULL is returned.  
  
### Remarks  
 This method makes it easy to traverse the tree without having to calculate position values beforehand.  
  
##  <a name="crbtree__getat"></a>  CRBTree::GetAt  
 Call this method to get the element at a given position in the tree.  
  
```  
  
CPair* GetAt(  
      POSITION  pos  
   ) throw( );  
   const CPair* GetAt(  
      POSITION  pos  
   ) const throw( );  
   void GetAt(  
      POSITION  pos,  
      KOUTARGTYPE  key,  
      VOUTARGTYPE  value  
   ) const;  
  
```  
  
### Parameters  
 `pos`  
 The position value.  
  
 `key`  
 The variable that receives the key.  
  
 *value*  
 The variable that receives the value.  
  
### Return Value  
 The first two forms return a pointer to a [CPair](../vs140/CRBTree--CPair-Class.md). The third form obtains a key and a value for the given position.  
  
### Remarks  
 The position value can be previously determined with a call to a method such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::GetTailPosition](../vs140/CRBTree--GetTailPosition.md).  
  
 In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
##  <a name="crbtree__getcount"></a>  CRBTree::GetCount  
 Call this method to get the number of elements in the tree.  
  
```  
  
size_t GetCount( ) const throw( );  
  
```  
  
### Return Value  
 Returns the number of elements (each key/value pair is one element) stored in the tree.  
  
##  <a name="crbtree__getheadposition"></a>  CRBTree::GetHeadPosition  
 Call this method to get the position value for the element at the head of the tree.  
  
```  
  
POSITION GetHeadPosition( ) const throw( );  
  
```  
  
### Return Value  
 Returns the position value for the element at the head of the tree.  
  
### Remarks  
 The value returned by `GetHeadPosition` can be used with methods such as [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md) or [CRBTree::GetNext](../vs140/CRBTree--GetNext.md) to traverse the tree and retrieve values.  
  
##  <a name="crbtree__getkeyat"></a>  CRBTree::GetKeyAt  
 Call this method to get the key from a given position in the tree.  
  
```  
  
const K& GetKeyAt(  
      POSITION  pos  
   ) const throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position value.  
  
### Return Value  
 Returns the key stored at position `pos` in the tree.  
  
### Remarks  
 If `pos` is not a valid position value, results are unpredictable. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
##  <a name="crbtree__getnext"></a>  CRBTree::GetNext  
 Call this method to obtain a pointer to an element stored in the `CRBTree` object, and advance the position to the next element.  
  
```  
  
const CPair* GetNext(  
      POSITION&  pos  
   ) const throw( );  
   CPair* GetNext(  
      POSITION&  pos  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Return Value  
 Returns a pointer to the next [CPair](../vs140/CRBTree--CPair-Class.md) value in the tree.  
  
### Remarks  
 The `pos` position counter is updated after each call. If the retrieved element is the last in the tree, `pos` is set to NULL.  
  
##  <a name="crbtree__getnextassoc"></a>  CRBTree::GetNextAssoc  
 Call this method to get the key and value of an element stored in the map and advance the position to the next element.  
  
```  
  
void GetNextAssoc(  
      POSITION&  pos,  
      KOUTARGTYPE  key,  
      VOUTARGTYPE  value  
   ) const;  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
 `key`  
 Template parameter specifying the type of the tree's key.  
  
 *value*  
 Template parameter specifying the type of the tree's value.  
  
### Remarks  
 The `pos` position counter is updated after each call. If the retrieved element is the last in the tree, `pos` is set to NULL.  
  
##  <a name="crbtree__getnextkey"></a>  CRBTree::GetNextKey  
 Call this method to get the key of an element stored in the tree and advance the position to the next element.  
  
```  
  
const K& GetNextKey(  
      POSITION&  pos  
   ) const throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Return Value  
 Returns a reference to the next key in the tree.  
  
### Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the tree, the position counter is set to NULL.  
  
##  <a name="crbtree__getnextvalue"></a>  CRBTree::GetNextValue  
 Call this method to get the value of an element stored in the tree and advance the position to the next element.  
  
```  
  
const V& GetNextValue(  
      POSITION&  pos  
   ) const throw( );  
   V& GetNextValue(  
      POSITION&  pos  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Return Value  
 Returns a reference to the next value in the tree.  
  
### Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the tree, the position counter is set to NULL.  
  
##  <a name="crbtree__getprev"></a>  CRBTree::GetPrev  
 Call this method to obtain a pointer to an element stored in the `CRBTree` object, and then update the position to the previous element.  
  
```  
  
const CPair* GetPrev(  
      POSITION&  pos  
   ) const throw( );  
   CPair* GetPrev(  
      POSITION&  pos  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Return Value  
 Returns a pointer to the previous [CPair](../vs140/CRBTree--CPair-Class.md) value stored in the tree.  
  
### Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the tree, the position counter is set to NULL.  
  
##  <a name="crbtree__gettailposition"></a>  CRBTree::GetTailPosition  
 Call this method to get the position value for the element at the tail of the tree.  
  
```  
  
POSITION GetTailPosition( ) const throw( );  
  
```  
  
### Return Value  
 Returns the position value for the element at the tail of the tree.  
  
### Remarks  
 The value returned by `GetTailPosition` can be used with methods such as [CRBTree::GetKeyAt](../vs140/CRBTree--GetKeyAt.md) or [CRBTree::GetPrev](../vs140/CRBTree--GetPrev.md) to traverse the tree and retrieve values.  
  
##  <a name="crbtree__getvalueat"></a>  CRBTree::GetValueAt  
 Call this method to retrieve the value stored at a given position in the `CRBTree` object.  
  
```  
  
const V& GetValueAt(  
      POSITION  pos  
   ) const throw( );  
   V& GetValueAt(  
      POSITION  pos  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Return Value  
 Returns a reference to the value stored at the given position in the `CRBTree` object.  
  
##  <a name="crbtree__isempty"></a>  CRBTree::IsEmpty  
 Call this method to test for an empty tree object.  
  
```  
  
bool IsEmpty( ) const throw( );  
  
```  
  
### Return Value  
 Returns **true** if the tree is empty,                         **false** otherwise.  
  
##  <a name="crbtree__kinargtype"></a>  CRBTree::KINARGTYPE  
 Type used when a key is passed as an input argument.  
  
```  
  
typedef KTraits::INARGTYPE KINARGTYPE;  
  
```  
  
##  <a name="crbtree__koutargtype"></a>  CRBTree::KOUTARGTYPE  
 Type used when a key is returned as an output argument.  
  
```  
  
typedef KTraits::OUTARGTYPE KOUTARGTYPE;  
  
```  
  
##  <a name="crbtree__removeall"></a>  CRBTree::RemoveAll  
 Call this method to remove all elements from the `CRBTree` object.  
  
```  
  
void RemoveAll( ) throw( );  
  
```  
  
### Remarks  
 Clears out the `CRBTree` object, freeing the memory used to store the elements.  
  
##  <a name="crbtree__removeat"></a>  CRBTree::RemoveAt  
 Call this method to remove the element at the given position in the **CRBTree** object.  
  
```  
  
void RemoveAt(  
      POSITION  pos  
   ) throw( );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
### Remarks  
 Removes the key/value pair stored at the specified position. The memory used to store the element is freed. The POSITION referenced by `pos` becomes invalid, and while the POSITION of any other elements in the tree remains valid, they do not necessarily retain the same order.  
  
##  <a name="crbtree__setvalueat"></a>  CRBTree::SetValueAt  
 Call this method to change the value stored at a given position in the `CRBTree` object.  
  
```  
  
void SetValueAt(  
      POSITION  pos,  
      VINARGTYPE  value  
   );  
  
```  
  
### Parameters  
 `pos`  
 The position counter, returned by a previous call to methods such as [CRBTree::GetHeadPosition](../vs140/CRBTree--GetHeadPosition.md) or [CRBTree::FindFirstKeyAfter](../vs140/CRBTree--FindFirstKeyAfter.md).  
  
 *value*  
 The value to add to the `CRBTree` object.  
  
### Remarks  
 Changes the value element stored at the given position in the `CRBTree` object.  
  
##  <a name="crbtree__vinargtype"></a>  CRBTree::VINARGTYPE  
 Type used when a value is passed as an input argument.  
  
```  
  
typedef VTraits::INARGTYPE VINARGTYPE;  
  
```  
  
##  <a name="crbtree__voutargtype"></a>  CRBTree::VOUTARGTYPE  
 Type used when a value is passed as an output argument.  
  
```  
  
typedef VTraits::OUTARGTYPE VOUTARGTYPE;  
  
```  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)