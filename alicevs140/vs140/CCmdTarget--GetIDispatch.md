---
title: "CCmdTarget::GetIDispatch"
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
ms.assetid: 96f48c6d-92c9-4344-96f9-2776e693c473
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::GetIDispatch
Call this member function to retrieve the `IDispatch` pointer from an automation method that either returns an `IDispatch` pointer or takes an `IDispatch` pointer by reference.  
  
## Syntax  
  
```  
  
      LPDISPATCH GetIDispatch(  
   BOOL bAddRef   
);  
```  
  
#### Parameters  
 *bAddRef*  
 Specifies whether to increment the reference count for the object.  
  
## Return Value  
 The `IDispatch` pointer associated with the object.  
  
## Remarks  
 For objects that call `EnableAutomation` in their constructors, making them automation enabled, this function returns a pointer to the Foundation Class implementation of `IDispatch` that is used by clients who communicate via the `IDispatch` interface. Calling this function automatically adds a reference to the pointer, so it is not necessary to make a call to [IUnknown::AddRef](http://msdn.microsoft.com/library/windows/desktop/ms691379).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::EnableAutomation](../vs140/CCmdTarget--EnableAutomation.md)   
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [IUnknown::Release](http://msdn.microsoft.com/library/windows/desktop/ms682317)