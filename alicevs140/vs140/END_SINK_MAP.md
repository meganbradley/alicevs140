---
title: "END_SINK_MAP"
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
ms.assetid: c8bb87a0-b224-46e5-9edc-fc4d7f1129b4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# END_SINK_MAP
Declares the end of the event sink map for the composite control.  
  
## Syntax  
  
```  
  
END_SINK_MAP( )  
  
```  
  
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
 [BEGIN_SINK_MAP](../vs140/BEGIN_SINK_MAP.md)   
 [SINK_ENTRY](../vs140/SINK_ENTRY.md)