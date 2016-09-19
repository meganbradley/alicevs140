---
title: "CObArray::Append"
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
ms.assetid: f2716ed0-d0b4-449a-b234-e6a4f9619934
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::Append
Call this member function to add the contents of another array to the end of the given array.  
  
## Syntax  
  
```  
  
      INT_PTR Append(  
   const CObArray& src   
);  
```  
  
#### Parameters  
 *src*  
 Source of the elements to be appended to the array.  
  
## Return Value  
 The index of the first appended element.  
  
## Remarks  
 The arrays must be of the same type.  
  
 If necessary, **Append** may allocate extra memory to accommodate the elements appended to the array.  
  
 The following table shows other member functions that are similar to `CObArray::Append`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**INT_PTR Append( const CByteArray&**  *src*  **);**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**INT_PTR Append( const CDWordArray&**  *src*  **);**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**INT_PTR Append( const CPtrArray&**  *src*  **);**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**INT_PTR Append( const CStringArray&**  *src*  **);**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**INT_PTR Append( const CUIntArray&**  *src*  **);**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**INT_PTR Append( const CWordArray&**  *src*  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#76](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#76)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::Copy](../vs140/CObArray--Copy.md)