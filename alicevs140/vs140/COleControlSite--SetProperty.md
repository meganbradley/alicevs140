---
title: "COleControlSite::SetProperty"
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
ms.assetid: 8882ee42-02b0-481b-a88c-c843f357cb42
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetProperty
Sets the control property specified by `dwDispID`.  
  
## Syntax  
  
```  
  
      virtual void AFX_CDECL SetProperty(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   ...   
);  
```  
  
#### Parameters  
 `dwDispID`  
 Identifies the dispatch ID of the property or method, found on the control's `IDispatch` interface, to be set.  
  
 `vtProp`  
 Specifies the type of property to be set. For possible values, see the Remarks section for [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md).  
  
 *...*  
 A single parameter of the type specified by `vtProp`.  
  
## Remarks  
 If `SetProperty` encounters an error, an exception is thrown.  
  
 The type of exception is determined by the return value of the attempt to set the property or method. If the return value is `DISP_E_EXCEPTION`, a **COleDispatchExcpetion** is thrown; otherwise a `COleException`.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::SetPropertyV](../vs140/COleControlSite--SetPropertyV.md)