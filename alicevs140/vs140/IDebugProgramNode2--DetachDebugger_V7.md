---
title: "IDebugProgramNode2::DetachDebugger_V7"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2d4b78e-a2dd-4217-97a6-ab648fd2ee2f
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramNode2::DetachDebugger_V7
DEPRECATED. DO NOT USE.  
  
## Syntax  
  
```cpp#  
HRESULT DetachDebugger_V7 (   
   void   
);  
```  
  
```c#  
int DetachDebugger_V7 ();  
```  
  
## Return Value  
 An implementation should always return `E_NOTIMPL`.  
  
## Remarks  
  
> [!WARNING]
>  As of [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)], this method is no longer used and should always return `E_NOTIMPL`.  
  
 This method is called when the debugger unexpectedly quits. When this method is called, the DE should resume the program as though the user detached from it. No more debug events should be sent. The program should be in a state where it is attachable from another instance of the debugger.  
  
## See Also  
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)