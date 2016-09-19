---
title: "CDHtmlDialog::GetControlProperty"
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
ms.assetid: 600393d9-d1f2-4bd4-80cd-a721c3286d0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetControlProperty
Retrieves the requested property of the specified ActiveX control.  
  
## Syntax  
  
```  
  
      VARIANT GetControlProperty(  
   LPCTSTR szId,  
   LPCTSTR szPropName   
);  
VARIANT GetControlProperty(  
   LPCTSTR szId,  
   DISPID dispid   
);  
VARIANT GetControlProperty(  
   IDispatch* pdispControl,  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `szId`  
 The HTML ID of an ActiveX control.  
  
 `szPropName`  
 The name of a property in the default locale of the current user.  
  
 `pdispControl`  
 The `IDispatch` pointer of an ActiveX control.  
  
 `dispid`  
 The dispatch ID of a property.  
  
## Return Value  
 A variant containing the requested property or an empty variant if the control or property could not be found.  
  
## Remarks  
 The overloads are listed from least efficient at the top to most efficient at the bottom.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetControlDispatch](../vs140/CDHtmlDialog--GetControlDispatch.md)