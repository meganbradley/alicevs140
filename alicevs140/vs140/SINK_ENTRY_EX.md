---
title: "SINK_ENTRY_EX"
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
ms.assetid: e1d14342-838f-4791-ac2f-5dae2801c1ac
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SINK_ENTRY_EX
Declares the handler function (`fn`) for the specified event (`dispid`), of the dispatch interface (*iid)*, for the control identified by `id`.  
  
## Syntax  
  
```  
  
      SINK_ENTRY_EX(   
   id,   
   iid,   
   dispid,   
   fn    
)  
```  
  
#### Parameters  
 `id`  
 [in] Identifies the control.  
  
 `iid`  
 [in] Identifies the dispatch interface.  
  
 `dispid`  
 [in] Identifies the specified event.  
  
 `fn`  
 [in] Name of the event handler function. This function must use the **_stdcall** calling convention and have the appropriate dispinterface-style signature.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#136](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#136)]  
  
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