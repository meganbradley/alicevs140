---
title: "IDebugModule3::LoadSymbols"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7548c8c1-cbc6-48aa-a845-19058d4a85bb
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule3::LoadSymbols
Loads the symbols for the current module.  
  
## Syntax  
  
```cpp#  
HRESULT LoadSymbols(  
   void  
);  
```  
  
```c#  
int LoadSymbols();  
```  
  
## Return Value  
 If the method succeeds, it returns `S_OK`. If it fails, it returns an error code.  
  
## Remarks  
 This method loads the symbols from the current search path (which can be altered by calling the [IDebugEngine3::SetSymbolPath](../vs140/IDebugEngine3--SetSymbolPath.md) method).  
  
 This method is preferred over the [IDebugModule2::ReloadSymbols_Deprecated](../vs140/IDebugModule2--ReloadSymbols_Deprecated.md) method.  
  
## See Also  
 [IDebugModule3](../vs140/IDebugModule3.md)   
 [IDebugEngine3::SetSymbolPath](../vs140/IDebugEngine3--SetSymbolPath.md)