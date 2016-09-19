---
title: "IDebugModule3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44f8e96e-9c59-4ffc-9a08-9c908a0e4de7
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule3
This interface represents a module that supports alternate locations of symbols and JustMyCode states.  
  
## Syntax  
  
```  
IDebugModule3 : IDebugModule2  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to support alternate locations of symbols and to work with JustMyCode states (see the [Visual Studio Debugging Glossary](../vs140/Visual-Studio-Debugger-Glossary.md) for a definition of "JustMyCode").  
  
## Notes for Callers  
 A call to [IDebugSymbolSearchEvent2::GetSymbolSearchInfo](../vs140/IDebugSymbolSearchEvent2--GetSymbolSearchInfo.md) returns this interface. The DE sends the [IDebugSymbolSearchEvent2](../vs140/IDebugSymbolSearchEvent2.md) interface to the session debug manager (SDM) using the [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md) method. Also, a call to [QueryInterface](../vs140/QueryInterface.md) on an [IDebugModule2](../vs140/IDebugModule2.md) interface returns this interface.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugModule2](../vs140/IDebugModule2.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetSymbolInfo](../vs140/IDebugModule3--GetSymbolInfo.md)|Returns a list of paths searched for symbols and the results of searching each path.|  
|[LoadSymbols](../vs140/IDebugModule3--LoadSymbols.md)|Loads and initializes symbols for the current module.|  
|[IsUserCode](../vs140/IDebugModule3--IsUserCode.md)|Returns flag specifying whether the module represents user code.|  
|[SetJustMyCodeState](../vs140/IDebugModule3--SetJustMyCodeState.md)|Specifies whether the module should be considered user code or not.|  
  
## Remarks  
 Visual Studio is the typical consumer of this interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugModule2](../vs140/IDebugModule2.md)   
 [IDebugSymbolSearchEvent2](../vs140/IDebugSymbolSearchEvent2.md)   
 [IDebugSymbolSearchEvent2::GetSymbolSearchInfo](../vs140/IDebugSymbolSearchEvent2--GetSymbolSearchInfo.md)