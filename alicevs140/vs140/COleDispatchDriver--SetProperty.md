---
title: "COleDispatchDriver::SetProperty"
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
ms.assetid: 2afb483c-3160-427f-80d6-0f8307a165ef
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::SetProperty
Sets the OLE object property specified by `dwDispID`.  
  
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
  
## Example  
 [!CODE [NVC_MFCOleContainer#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#7)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md)   
 [COleDispatchDriver::GetProperty](../vs140/COleDispatchDriver--GetProperty.md)