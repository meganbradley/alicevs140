---
title: "COleControl::OnGetDisplayString"
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
ms.assetid: 405f6f9d-b28b-4908-abc5-4e104219f513
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnGetDisplayString
Called by the framework to obtain a string that represents the current value of the property identified by `dispid`.  
  
## Syntax  
  
```  
  
      virtual BOOL OnGetDisplayString(  
   DISPID dispid,  
   CString& strValue   
);  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 `strValue`  
 A reference to a [CString](../vs140/CStringT-Class.md) object through which a string will be returned.  
  
## Return Value  
 Nonzero if a string has been returned in *strValue;* otherwise 0.  
  
## Remarks  
 Override this function if your control has a property whose value cannot be directly converted to a string and you want the property's value to be displayed in a container-supplied property browser.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnMapPropertyToPage](../vs140/COleControl--OnMapPropertyToPage.md)