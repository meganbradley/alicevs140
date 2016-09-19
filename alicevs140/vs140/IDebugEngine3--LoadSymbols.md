---
title: "IDebugEngine3::LoadSymbols"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c846a440-1d91-4d48-b8f1-82e902ae152b
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine3::LoadSymbols
Loads (as necessary) symbols for all modules being debugged by this debugging engine.  
  
## Syntax  
  
```cpp  
HRESULT LoadSymbols();  
```  
  
```c#  
int LoadSymbols();  
```  
  
#### Parameters  
 None.  
  
## Return Value  
 If successful, returns S_OK; otherwise returns error code.  
  
## Remarks  
 This loads debugging symbols for all modules referenced by this debugging engine. The symbols are loaded only if they have not already been loaded. Symbols are searched on the paths set by a call to [IDebugEngine3::SetSymbolPath](../vs140/IDebugEngine3--SetSymbolPath.md).  
  
## See Also  
 [IDebugEngine3::SetSymbolPath](../vs140/IDebugEngine3--SetSymbolPath.md)   
 [IDebugEngine3](../vs140/IDebugEngine3.md)