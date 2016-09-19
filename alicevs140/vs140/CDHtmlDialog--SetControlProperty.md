---
title: "CDHtmlDialog::SetControlProperty"
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
ms.assetid: c76e24d3-6037-4650-86bb-b884f370d55c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::SetControlProperty
Sets the property of an ActiveX control to a new value.  
  
## Syntax  
  
```  
  
      void SetControlProperty(  
   LPCTSTR szElementId,  
   DISPID dispid,  
   VARIANT *pVar   
);  
void SetControlProperty(  
   IDispatch *pdispControl,  
   DISPID dispid,  
   VARIANT *pVar  
);  
void SetControlProperty(  
   LPCTSTR szElementId,  
   LPCTSTR szPropName,  
   VARIANT *pVar  
);  
```  
  
#### Parameters  
 `szElementId`  
 The HTML ID of an ActiveX control.  
  
 `dispid`  
 The dispatch ID of the property to set.  
  
 *pVar*  
 Pointer to a **VARIANT** containing the new property value.  
  
 `pdispControl`  
 Pointer to an ActiveX control's `IDispatch` interface.  
  
 `szPropName`  
 String containing the name of the property to set.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::SetElementProperty](../vs140/CDHtmlDialog--SetElementProperty.md)