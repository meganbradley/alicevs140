---
title: "COleControlSite::SetPropertyV"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a1ff585e-8a00-40e4-81f1-85fc96281c35
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetPropertyV
Sets the control property specified by `dwDispID`.  
  
## Syntax  
  
```  
  
      virtual void SetPropertyV(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   va_list argList   
);  
```  
  
#### Parameters  
 `dwDispID`  
 Identifies the dispatch ID of the property or method, found on the control's `IDispatch` interface, to be set.  
  
 `vtProp`  
 Specifies the type of property to be set. For possible values, see the Remarks section for [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md).  
  
 `argList`  
 Pointer to the list of arguments.  
  
## Remarks  
 Extra parameters for the method or property being invoked can be passeed using the *arg_list* parameter. If `SetProperty` encounters an error, an exception is thrown.  
  
 The type of exception is determined by the return value of the attempt to set the property or method. If the return value is `DISP_E_EXCEPTION`, a **COleDispatchExcpetion** is thrown; otherwise a `COleException`.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::SetProperty](../vs140/COleControlSite--SetProperty.md)