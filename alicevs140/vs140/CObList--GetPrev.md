---
title: "CObList::GetPrev"
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
ms.assetid: 674a4712-d3b4-4bae-8fc4-9e6ec4c47981
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetPrev
Gets the list element identified by `rPosition`, then sets `rPosition` to the `POSITION` value of the previous entry in the list.  
  
## Syntax  
  
```  
CObject*& GetPrev(  
   POSITION& rPosition   
);  
const CObject* GetPrev(  
   POSITION& rPosition   
) const;  
```  
  
#### Parameters  
 `rPosition`  
 A reference to a `POSITION` value returned by a previous `GetPrev` or other member function call.  
  
## Return Value  
 See the return value description for [GetHead](../vs140/CObList--GetHead.md).  
  
## Remarks  
 You can use `GetPrev` in a reverse iteration loop if you establish the initial position with a call to `GetTailPosition` or `Find`.  
  
 You must ensure that your `POSITION` value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
 If the retrieved element is the first in the list, then the new value of `rPosition` is set to `NULL`.  
  
> [!NOTE]
>  As of MFC 8.0 the const version of this method has changed to return `const CObject*` instead of `const CObject*&`.  This change was made to bring the compiler into conformance with the C++ standard.  
  
 The following table shows other member functions that are similar to `CObList::GetPrev`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|`void*& GetPrev( POSITION&`  `rPosition`  `);`<br /><br /> `const void* GetPrev( POSITION&`  `rPosition`  `) const;`|  
|[CStringList](../vs140/CStringList-Class.md)|`CString& GetPrev( POSITION&`  `rPosition`  `);`<br /><br /> `const CString& GetPrev( POSITION&`  `rPosition`  `) const;`|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#99](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#99)]  
  
 The results from this program are as follows:  
  
 `a CAge at $421C 21`  
  
 `a CAge at $421C 40`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::GetTailPosition](../vs140/CObList--GetTailPosition.md)   
 [CObList::GetHeadPosition](../vs140/CObList--GetHeadPosition.md)   
 [CObList::GetNext](../vs140/CObList--GetNext.md)   
 [CObList::GetHead](../vs140/CObList--GetHead.md)