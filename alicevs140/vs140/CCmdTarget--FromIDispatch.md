---
title: "CCmdTarget::FromIDispatch"
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
ms.assetid: adf089dd-edf0-4841-a075-15cbaa76c8d4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::FromIDispatch
Call this function to map an `IDispatch` pointer, received from automation member functions of a class, into the `CCmdTarget` object that implements the interfaces of the `IDispatch` object.  
  
## Syntax  
  
```  
  
      static CCmdTarget* PASCAL FromIDispatch(  
   LPDISPATCH lpDispatch   
);  
```  
  
#### Parameters  
 `lpDispatch`  
 A pointer to an `IDispatch` object.  
  
## Return Value  
 A pointer to the `CCmdTarget` object associated with `lpDispatch`. This function returns **NULL** if the `IDispatch` object is not recognized as a Microsoft Foundation Class `IDispatch` object.  
  
## Remarks  
 The result of this function is the inverse of a call to the member function `GetIDispatch`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::GetIDispatch](../vs140/CCmdTarget--GetIDispatch.md)   
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)