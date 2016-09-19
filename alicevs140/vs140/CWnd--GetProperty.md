---
title: "CWnd::GetProperty"
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
ms.assetid: 66e814bd-ee55-46a0-a385-927546df6268
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetProperty
Call this member function to get the ActiveX control property specified by `dwDispID`.  
  
## Syntax  
  
```  
  
      void GetProperty(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   void* pvProp   
)const;  
```  
  
#### Parameters  
 `dwDispID`  
 Identifies the property to be retrieved.  
  
 `vtProp`  
 Specifies the type of the property to be retrieved. For possible values, see the Remarks section for [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md).  
  
 `pvProp`  
 Address of the variable that will that will receive the property value. It must match the type specified by `vtProp`.  
  
## Remarks  
 **GetProperty** returns the value through `pvProp`.  
  
> [!NOTE]
>  This function should be called only on a `CWnd` object that represents an ActiveX control.  
  
 For more information about using this member function with ActiveX Control Containers, see the article [ActiveX Control Containers: Programming ActiveX Controls in an ActiveX Control Container](../vs140/ActiveX-Control-Containers--Programming-ActiveX-Controls-in-an-ActiveX-Control-Container.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::InvokeHelper](../vs140/CWnd--InvokeHelper.md)   
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [CWnd::CreateControl](../vs140/CWnd--CreateControl.md)