---
title: "CSimpleArray Class"
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
ms.assetid: ee0c9f39-b61c-4c18-bc43-4eada21dca3a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray Class
This class provides methods for managing a simple array.  
  
## Syntax  
  
```  
  
template <class T,  
      class  TEqual  
    = CSimpleArrayEqualHelper<  T  
    >  
   >   
   class CSimpleArray  
  
```  
  
#### Parameters  
 `T`  
 The type of data to store in the array.  
  
 `TEqual`  
 A trait object, defining the equality test for elements of type `T`.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleArray::CSimpleArray](../vs140/CSimpleArray--CSimpleArray.md)|The constructor for the simple array.|  
|[CSimpleArray::~CSimpleArray](../vs140/CSimpleArray--~CSimpleArray.md)|The destructor for the simple array.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleArray::Add](../vs140/CSimpleArray--Add.md)|Adds a new element to the array.|  
|[CSimpleArray::Find](../vs140/CSimpleArray--Find.md)|Finds an element in the array.|  
|[CSimpleArray::GetData](../vs140/CSimpleArray--GetData.md)|Returns a pointer to the data stored in the array.|  
|[CSimpleArray::GetSize](../vs140/CSimpleArray--GetSize.md)|Returns the number of elements stored in the array.|  
|[CSimpleArray::Remove](../vs140/CSimpleArray--Remove.md)|Removes a given element from the array.|  
|[CSimpleArray::RemoveAll](../vs140/CSimpleArray--RemoveAll.md)|Removes all elements from the array.|  
|[CSimpleArray::RemoveAt](../vs140/CSimpleArray--RemoveAt.md)|Removes the specified element from the array.|  
|[CSimpleArray::SetAtIndex](../vs140/CSimpleArray--SetAtIndex.md)|Sets the specified element in the array.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleArray::operator &#91;&#93;](../vs140/CSimpleArray--operator.md)|Retrieves an element from the array.|  
|[CSimpleArray::operator =](../vs140/CSimpleArray--operator-=.md)|Assignment operator.|  
  
## Remarks  
 `CSimpleArray` provides methods for creating and managing a simple array, of any given type `T`.  
  
 The parameter `TEqual` provides a means of defining an equality function for two elements of type `T`. By creating a class similar to [CSimpleArrayEqualHelper](../vs140/CSimpleArrayEqualHelper-Class.md), it is possible to alter the behavior of the equality test for any given array. For example, when dealing with an array of pointers, it may be useful to define the equality as depending on the values the pointers reference. The default implementation utilizes **operator=()**.  
  
 Both `CSimpleArray` and [CSimpleMap](../vs140/CSimpleMap-Class.md) are designed for a small number of elements. [CAtlArray](../vs140/CAtlArray-Class.md) and [CAtlMap](../vs140/CAtlMap-Class.md) should be used when the array contains a large number of elements.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## Example  
 [!CODE [NVC_ATL_Utilities#86](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#86)]  
  
##  <a name="csimplearray__add"></a>  CSimpleArray::Add  
 Adds a new element to the array.  
  
```  
  
BOOL Add(  
      const T&  t  
   );  
  
```  
  
### Parameters  
 *t*  
 The element to add to the array.  
  
### Return Value  
 Returns TRUE if the element is successfully added to the array, FALSE otherwise.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#87](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#87)]  
  
##  <a name="csimplearray__csimplearray"></a>  CSimpleArray::CSimpleArray  
 The constructor for the array object.  
  
```  
  
CSimpleArray(  
      const CSimpleArray< T, TEqual >&  src  
   );  
   CSimpleArray( );  
  
```  
  
### Parameters  
 *src*  
 An existing `CSimpleArray` object.  
  
### Remarks  
 Initializes the data members, creating a new empty `CSimpleArray` object, or a copy of an existing `CSimpleArray` object.  
  
##  <a name="csimplearray___dtorcsimplearray"></a>  CSimpleArray::~CSimpleArray  
 The destructor.  
  
```  
  
~CSimpleArray( );  
  
```  
  
### Remarks  
 Frees all allocated resources.  
  
##  <a name="csimplearray__find"></a>  CSimpleArray::Find  
 Finds an element in the array.  
  
```  
  
int Find(  
      const T&  t  
   ) const;  
  
```  
  
### Parameters  
 *t*  
 The element for which to search.  
  
### Return Value  
 Returns the index of the found element, or -1 if the element is not found.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#88](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#88)]  
  
##  <a name="csimplearray__getdata"></a>  CSimpleArray::GetData  
 Returns a pointer to the data stored in the array.  
  
```  
  
T* GetData( ) const;  
  
```  
  
### Return Value  
 Returns a pointer to the data in the array.  
  
##  <a name="csimplearray__getsize"></a>  CSimpleArray::GetSize  
 Returns the number of elements stored in the array.  
  
```  
  
int GetSize( ) const;  
  
```  
  
### Return Value  
 Returns the number of elements stored in the array.  
  
##  <a name="csimplearray__operator__at"></a>  CSimpleArray::operator []  
 Retrieves an element from the array.  
  
```  
  
T& operator[](int  nIndex);  
  
```  
  
### Parameters  
 `nIndex`  
 The element index.  
  
### Return Value  
 Returns the element of the array referenced by `nIndex`.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#89](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#89)]  
  
##  <a name="csimplearray__operator__eq"></a>  CSimpleArray::operator =  
 Assignment operator.  
  
```  
  
CSimpleArray< T, TEqual >  
   & operator =(  
      const CSimpleArray< T, TEqual >&  src  
   );  
  
```  
  
### Parameters  
 *src*  
 The array to copy.  
  
### Return Value  
 Returns a pointer to the updated `CSimpleArray` object.  
  
### Remarks  
 Copies all elements from the `CSimpleArray` object referenced by *src* into the current array object, replacing all existing data.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#90](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#90)]  
  
##  <a name="csimplearray__remove"></a>  CSimpleArray::Remove  
 Removes a given element from the array.  
  
```  
  
BOOL Remove(  
      const T&  t  
   );  
  
```  
  
### Parameters  
 *t*  
 The element to remove from the array.  
  
### Return Value  
 Returns TRUE if the element is found and removed, FALSE otherwise.  
  
### Remarks  
 When an element is removed, the remaining elements in the array are renumbered to fill the empty space.  
  
##  <a name="csimplearray__removeall"></a>  CSimpleArray::RemoveAll  
 Removes all elements from the array.  
  
```  
  
void RemoveAll( );  
  
```  
  
### Remarks  
 Removes all elements currently stored in the array.  
  
##  <a name="csimplearray__removeat"></a>  CSimpleArray::RemoveAt  
 Removes the specified element from the array.  
  
```  
  
BOOL RemoveAt(  
      int  nIndex  
   );  
  
```  
  
### Parameters  
 `nIndex`  
 Index pointing to the element to remove.  
  
### Return Value  
 Returns TRUE if the element was removed, FALSE if the index was invalid.  
  
### Remarks  
 When an element is removed, the remaining elements in the array are renumbered to fill the empty space.  
  
##  <a name="csimplearray__setatindex"></a>  CSimpleArray::SetAtIndex  
 Set the specified element in the array.  
  
```  
  
BOOL SetAtIndex(  
      int  nIndex,  
      const T&  t  
   );  
  
```  
  
### Parameters  
 `nIndex`  
 The index of the element to change.  
  
 *t*  
 The value to assign to the specified element.  
  
### Return Value  
 Returns TRUE if successful, FALSE if the index was not valid.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)