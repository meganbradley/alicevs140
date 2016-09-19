---
title: "CObArray::SetAt"
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
ms.assetid: 4e5e8ceb-fe1e-4d4b-a650-8a16715e280a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::SetAt
Sets the array element at the specified index.  
  
## Syntax  
  
```  
  
      void SetAt(  
   INT_PTR nIndex,  
   CObject* newElement   
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `GetUpperBound`.  
  
 `newElement`  
 The object pointer to be inserted in this array. A **NULL** value is allowed.  
  
## Remarks  
 `SetAt` will not cause the array to grow. Use `SetAtGrow` if you want the array to grow automatically.  
  
 You must ensure that your index value represents a valid position in the array. If it is out of bounds, then the Debug version of the library asserts.  
  
 The following table shows other member functions that are similar to `CObArray::SetAt`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, BYTE**  `newElement`  **);**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, DWORD**  `newElement`  **);**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, void\***  `newElement`  **);**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, LPCTSTR**  `newElement`  **);**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, UINT**  `newElement`  **);**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**void SetAt( INT_PTR** `nIndex` **, WORD**  `newElement`  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#86](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#86)]  
  
 The results from this program are as follows:  
  
 `SetAt example: A CObArray with 2 elements`  
  
 `[0] = a CAge at $47E0 30`  
  
 `[1] = a CAge at $47A0 40`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetAt](../vs140/CObArray--GetAt.md)   
 [CObArray::SetAtGrow](../vs140/CObArray--SetAtGrow.md)   
 [CObArray::ElementAt](../vs140/CObArray--ElementAt.md)   
 [CObArray::operator](../vs140/CObArray--operator.md)