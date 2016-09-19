---
title: "CCmdTarget::IsInvokeAllowed"
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
ms.assetid: 975d26e2-1a61-4993-9675-8d511ff37fe6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::IsInvokeAllowed
This function is called by MFC's implementation of **IDispatch::Invoke** to determine if a given automation method (identified by `dispid`) can be invoked.  
  
## Syntax  
  
```  
  
      virtual BOOL IsInvokeAllowed(  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `dispid`  
 A dispatch ID.  
  
## Return Value  
 TRUE if the method can be invoked, otherwise FALSE.  
  
## Remarks  
 If `IsInvokeAllowed` returns TRUE, **Invoke** proceeds to call the method; otherwise, `Invoke` will fail, returning E_UNEXPECTED.  
  
 Derived classes can override this function to return appropriate values (if not overridden, `IsInvokeAllowed` returns TRUE). See in particular [COleControl::IsInvokeAllowed](../vs140/COleControl--IsInvokeAllowed.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::IsInvokeAllowed](../vs140/COleControl--IsInvokeAllowed.md)