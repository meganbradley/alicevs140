---
title: "IDebugEngine3::SetAllExceptions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f03a6ac-a854-42f7-933c-a2df1b351975
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine3::SetAllExceptions
This method sets the state of all outstanding exceptions.  
  
## Syntax  
  
```cpp  
HRESULT SetAllExceptions(  
   EXCEPTION_STATE dwState  
);  
```  
  
```c#  
int SetAllExceptions(  
   enum_EXCEPTION_STATE dwState  
);  
```  
  
#### Parameters  
 `dwState`  
 [in] One of the [EXCEPTION_STATE](../vs140/EXCEPTION_STATE.md) values.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDebugEngine3](../vs140/IDebugEngine3.md)   
 [EXCEPTION_STATE](../vs140/EXCEPTION_STATE.md)