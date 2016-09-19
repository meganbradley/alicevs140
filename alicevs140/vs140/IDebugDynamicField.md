---
title: "IDebugDynamicField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: caffbd95-7596-4714-84b1-b964e89a78bb
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDynamicField
This interface represents a type of a variable.  
  
## Syntax  
  
```  
IDebugDynamicField : IDebugField  
```  
  
## Notes for Implementers  
 This interface is implemented by symbol providers as a base class for any type that can be determined at run time. This is for managed code only.  
  
## Notes for Callers  
 This interface represents a base class from which more specialized interfaces can be derived.  
  
## Methods in Vtable order  
 This interface does not supply any methods other than those inherited from `IDebugField`.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugField](../vs140/IDebugField.md)