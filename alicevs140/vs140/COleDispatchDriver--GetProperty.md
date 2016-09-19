---
title: "COleDispatchDriver::GetProperty"
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
ms.assetid: 088d7494-7c94-4969-9558-22af8ce34ea7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::GetProperty
Gets the object property specified by `dwDispID`.  
  
## Syntax  
  
```  
  
      void GetProperty(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   void* pvProp   
) const;  
```  
  
#### Parameters  
 `dwDispID`  
 Identifies the property to be retrieved.  
  
 `vtProp`  
 Specifies the property to be retrieved. For possible values, see the Remarks section for [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md).  
  
 `pvProp`  
 Address of the variable that will receive the property value. It must match the type specified by `vtProp`.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#6)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::InvokeHelper](../vs140/COleDispatchDriver--InvokeHelper.md)   
 [COleDispatchDriver::SetProperty](../vs140/COleDispatchDriver--SetProperty.md)