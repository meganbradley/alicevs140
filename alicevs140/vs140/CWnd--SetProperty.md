---
title: "CWnd::SetProperty"
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
ms.assetid: 9f42cb90-c27e-41a4-ad62-b3ead53a5aca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetProperty
Call this member function to set the OLE control property specified by `dwDispID`.  
  
## Syntax  
  
```  
  
      void AFX_CDECL SetProperty(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   ...   
);  
```  
  
#### Parameters  
 `dwDispID`  
 Identifies the property to be set.  
  
 `vtProp`  
 Specifies the type of the property to be set. For possible values, see the Remarks section for [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md).  
  
 *...*  
 A single parameter of the type specified by `vtProp`.  
  
## Remarks  
  
> [!NOTE]
>  This function should be called only on a `CWnd` object that represents an OLE control.  
  
 For more information about using this member function with OLE Control Containers, see the article [ActiveX Control Containers: Programming ActiveX Controls in an ActiveX Control Container](../vs140/ActiveX-Control-Containers--Programming-ActiveX-Controls-in-an-ActiveX-Control-Container.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::InvokeHelper](../vs140/CWnd--InvokeHelper.md)   
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [CWnd::CreateControl](../vs140/CWnd--CreateControl.md)