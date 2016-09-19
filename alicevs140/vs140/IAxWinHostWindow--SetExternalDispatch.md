---
title: "IAxWinHostWindow::SetExternalDispatch"
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
ms.assetid: 68e24362-96b5-44ae-aa6b-9a021b4ecce9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindow::SetExternalDispatch
Sets the external dispinterface, which is available to contained controls through the [IDocHostUIHandlerDispatch::GetExternal](../vs140/IDocHostUIHandlerDispatch-Interface.md) method.  
  
## Syntax  
  
```  
  
      STDMETHOD( SetExternalDispatch )(  
   IDispatch* pDisp   
);  
```  
  
#### Parameters  
 `pDisp`  
 [in] A pointer to an `IDispatch` interface.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindow Interface](../vs140/IAxWinHostWindow-Interface.md)   
 [CAxWindow::SetExternalDispatch](../vs140/CAxWindow--SetExternalDispatch.md)