---
title: "IDebugWindowsComputerPort2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 25f327b8-0303-4268-88d1-74df630436aa
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugWindowsComputerPort2
Allows querying for information about the target computer.  
  
## Syntax  
  
```  
IDebugWindowsComputerPort2 : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by port objects of the session debug manager.  
  
## Methods  
 The following table shows the methods of `IDebugWindowsComputerPort2`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugWindowsComputerPort2::GetComputerInfo](../vs140/IDebugWindowsComputerPort2--GetComputerInfo.md)|Retrieves information about the computer on which the debugger in running.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll