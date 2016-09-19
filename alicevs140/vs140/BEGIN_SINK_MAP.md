---
title: "BEGIN_SINK_MAP"
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
ms.assetid: 32542b3d-ac43-4139-8ac4-41c48481744f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_SINK_MAP
Declares the beginning of the event sink map for the composite control.  
  
## Syntax  
  
```  
  
BEGIN_SINK_MAP( _class )  
```  
  
#### Parameters  
 `_class`  
 [in] Specifies the control.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#104](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#104)]  
  
## Remarks  
 CE ATL implementation of ActiveX event sinks only supports return values of type HRESULT or void from your event handler methods; any other return value is unsupported and its behavior is undefined.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Composite Control Macros](../vs140/Composite-Control-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)   
 [SINK_ENTRY](../vs140/SINK_ENTRY.md)   
 [END_SINK_MAP](../vs140/END_SINK_MAP.md)