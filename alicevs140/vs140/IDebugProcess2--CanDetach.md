---
title: "IDebugProcess2::CanDetach"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2830f7c3-69fb-474a-97b8-5b869e38d546
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::CanDetach
Determines if the session debug manager (SDM) can detach the process.  
  
## Syntax  
  
```cpp#  
HRESULT CanDetach(  
   void  
);  
```  
  
```c#  
int CanDetach();  
```  
  
## Return Value  
 If successful, returns `S_OK.` Returns `S_FALSE` if the debugger cannot detach from the process. Otherwise, returns an error code.  
  
## See Also  
 [CanDetach](../vs140/IDebugProgram2--CanDetach.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)