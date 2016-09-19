---
title: "CObList::InsertAfter"
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
ms.assetid: 6b7258b1-467d-45b7-ba89-0fdbc01d5f4b
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::InsertAfter
Adds an element to this list after the element at the specified position.  
  
## Syntax  
  
```  
  
      POSITION InsertAfter(  
   POSITION position,  
   CObject* newElement   
);  
```  
  
#### Parameters  
 *position*  
 A **POSITION** value returned by a previous `GetNext`, `GetPrev`, or **Find** member function call.  
  
 `newElement`  
 The object pointer to be added to this list.  
  
 The following table shows other member functions that are similar to `CObList::InsertAfter`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION InsertAfter( POSITION**  *position* **, void\***  `newElement`  **);**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION InsertAfter( POSITION**  *position* **, const CString&**  `newElement`  **);**<br /><br /> **POSITION InsertAfter( POSITION**  *position* **, LPCTSTR**  `newElement`  **);**|  
  
## Return Value  
 A **POSITION** value which is the same as the *position* parameter.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#103](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#103)]  
  
 The results from this program are as follows:  
  
 `InsertAfter example: A CObList with 3 elements`  
  
 `a CAge at $4A44 40`  
  
 `a CAge at $4A64 65`  
  
 `a CAge at $4968 21`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::InsertBefore](../vs140/CObList--InsertBefore.md)