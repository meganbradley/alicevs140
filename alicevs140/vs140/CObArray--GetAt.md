---
title: "CObArray::GetAt"
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
ms.assetid: d020a31e-f07a-483b-8d10-8efa8701f8f3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::GetAt
Returns the array element at the specified index.  
  
## Syntax  
  
```  
  
      CObject* GetAt(  
   INT_PTR nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `GetUpperBound`.  
  
## Return Value  
 The `CObject` pointer element currently at this index.  
  
## Remarks  
  
> [!NOTE]
>  Passing a negative value or a value greater than the value returned by `GetUpperBound` will result in a failed assertion.  
  
 The following table shows other member functions that are similar to `CObArray::GetAt`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**BYTE GetAt( INT_PTR** `nIndex` **) const;**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**DWORD GetAt( INT_PTR** `nIndex` **) const;**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void\* GetAt( INT_PTR** `nIndex` **) const;**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**CString GetAt( INT_PTR** `nIndex` **) const;**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**UINT GetAt( INT_PTR** `nIndex` **) const;**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**WORD GetAt( INT_PTR** `nIndex` **) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#79](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#79)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::SetAt](../vs140/CObArray--SetAt.md)   
 [CObArray::operator](../vs140/CObArray--operator.md)