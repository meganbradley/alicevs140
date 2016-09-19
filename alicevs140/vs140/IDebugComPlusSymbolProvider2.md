---
title: "IDebugComPlusSymbolProvider2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa2f9b49-03ad-43c7-92d6-6dcb9c3d0531
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugComPlusSymbolProvider2
Represents a COM+ symbol provider with methods that are specific to managed code and extends the **IDebugComPlusSymbolProvider**[](../vs140/IDebugComPlusSymbolProvider.md "IDebugComPlusSymbolProvider").  
  
## Syntax  
  
```  
IDebugComPlusSymbolProvider2 : IDebugComPlusSymbolProvider  
```  
  
## Methods  
 In addition to the methods on the [IDebugComPlusSymbolProvider](../vs140/IDebugComPlusSymbolProvider.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugComPlusSymbolProvider2::FunctionHasLineInfo](../vs140/IDebugComPlusSymbolProvider2--FunctionHasLineInfo.md)|Determines if the specified method has line information.|  
|[IDebugComPlusSymbolProvider2::GetTypesByName](../vs140/IDebugComPlusSymbolProvider2--GetTypesByName.md)|Retrieves a type given its name.|  
|[IDebugComPlusSymbolProvider2::GetTypeFromToken](../vs140/IDebugComPlusSymbolProvider2--GetTypeFromToken.md)|Retrieves a type given its token.|  
|[IDebugComPlusSymbolProvider2::IsAddressSequencePoint](../vs140/IDebugComPlusSymbolProvider2--IsAddressSequencePoint.md)|Determines if the specified debug address is a sequence point.|  
|[IDebugComPlusSymbolProvider2::LoadSymbolsFromCallback](../vs140/IDebugComPlusSymbolProvider2--LoadSymbolsFromCallback.md)|Loads debug symbols using the specified callback method.|  
|[IDebugComPlusSymbolProvider2::LoadSymbolsFromStreamWithCorModule](../vs140/IDebugComPlusSymbolProvider2--LoadSymbolsFromStreamWithCorModule.md)|Load debug symbols from a data stream given the **ICorDebugModule** object.|  
|[IDebugComPlusSymbolProvider2::LoadSymbolsWithCorModule](../vs140/IDebugComPlusSymbolProvider2--LoadSymbolsWithCorModule.md)|Loads debug symbols given the **ICorDebugModule** object.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll