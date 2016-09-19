---
title: "CTypedPtrList::SetAt"
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
ms.assetid: 534cc580-5db4-4d2a-81a9-18785b57b9d5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrList::SetAt
This member function calls `BASE_CLASS`**::SetAt**.  
  
## Syntax  
  
```  
  
      void SetAt(  
   POSITION pos,  
   TYPE newElement   
);  
```  
  
#### Parameters  
 `pos`  
 The **POSITION** of the element to be set.  
  
 *TYPE*  
 Type of the elements stored in the base-class list.  
  
 `newElement`  
 The object pointer to be written to the list.  
  
## Remarks  
 A variable of type **POSITION** is a key for the list. It is not the same as an index, and you cannot operate on a **POSITION** value yourself. `SetAt` writes the object pointer to the specified position in the list.  
  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
 For more detailed remarks, see [CObList::SetAt](../vs140/CObList--SetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)