---
title: "COlePropertyPage::GetObjectArray"
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
ms.assetid: 85f9dd20-a4fd-4246-b0e3-8e4fda0b1c9e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::GetObjectArray
Returns the array of objects being edited by the property page.  
  
## Syntax  
  
```  
  
      LPDISPATCH* GetObjectArray(  
   ULONG* pnObjects   
);  
```  
  
#### Parameters  
 `pnObjects`  
 Pointer to an unsigned long integer that will receive the number of objects being edited by the page.  
  
## Return Value  
 Pointer to an array of `IDispatch` pointers, which are used to access the properties of each control on the property page. The caller must not release these interface pointers.  
  
## Remarks  
 Each property page object maintains an array of pointers to the `IDispatch` interfaces of the objects being edited by the page. This function sets its `pnObjects` argument to the number of elements in that array and returns a pointer to the first element of the array.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)