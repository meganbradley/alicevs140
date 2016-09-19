---
title: "CObArray::operator"
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
ms.assetid: 0070f322-5e20-44f3-b45d-f337efdfae2c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::operator
These subscript operators are a convenient substitute for the `SetAt` and `GetAt` functions.  
  
## Syntax  
  
```  
  
      CObject*& operator [](INT_PTR nIndex);  
CObject* operator [](INT_PTR nIndex) const;  
```  
  
## Remarks  
 The first operator, called for arrays that are not **const**, may be used on either the right (r-value) or the left (l-value) of an assignment statement. The second, called for **const** arrays, may be used only on the right.  
  
 The Debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.  
  
 The following table shows other operators that are similar to **CObArray::operator []**.  
  
|Class|Operator|  
|-----------|--------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**BYTE& operator [](INT_PTR** `nIndex`  **\);**<br /><br /> **BYTE operator [](INT_PTR**  `nIndex`  **\) const;**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**DWORD& operator [](INT_PTR**  `nIndex`  **\);**<br /><br /> **DWORD operator [](INT_PTR**  `nIndex`  **\) const;**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void\*& operator [](INT_PTR**  `nIndex`  **\);**<br /><br /> **void\* operator [](INT_PTR**  `nIndex`  **\) const;**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**CString& operator [](INT_PTR**  `nIndex`  **\);**<br /><br /> **CString operator [](INT_PTR**  `nIndex`  **\) const;**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**UINT& operator [](INT_PTR**  `nIndex`  **\);**<br /><br /> **UINT operator [](INT_PTR**  `nIndex`  **\) const;**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**WORD& operator [](INT_PTR**  `nIndex`  **\);**<br /><br /> **WORD operator [](INT_PTR**  `nIndex`  **\) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#88](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#88)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetAt](../vs140/CObArray--GetAt.md)   
 [CObArray::SetAt](../vs140/CObArray--SetAt.md)