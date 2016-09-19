---
title: "ON_REGISTERED_THREAD_MESSAGE"
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
ms.topic: article
ms.assetid: 3f598bc2-b2f0-410f-8ba0-7714502170f3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_REGISTERED_THREAD_MESSAGE
Indicates which function will handle the message registered by the Windows **RegisterWindowMessage** function.  
  
## Syntax  
  
```  
  
ON_REGISTERED_THREAD_MESSAGE(  
nMessageVariable  
,   
memberFxn )  
```  
  
#### Parameters  
 `nMessageVariable`  
 The registered window-message ID variable.  
  
 `memberFxn`  
 The name of the `CWinThread`-message-handler function to which the message is mapped.  
  
## Remarks  
 **RegisterWindowMessage** is used to define a new window message that is guaranteed to be unique throughout the system. `ON_REGISTERED_THREAD_MESSAGE` must be used instead of `ON_REGISTERED_MESSAGE` when you have a `CWinThread` class.  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_REGISTERED_MESSAGE](../vs140/ON_REGISTERED_MESSAGE.md)   
 [ON_THREAD_MESSAGE](../vs140/ON_THREAD_MESSAGE.md)   
 [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947)   
 [CWinThread Class](../vs140/CWinThread-Class.md)