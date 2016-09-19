---
title: "CWinThread::ProcessMessageFilter"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f867a047-1285-45da-8fb3-c745cfab5e1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::ProcessMessageFilter
The framework's hook function calls this member function to filter and respond to certain Windows messages.  
  
## Syntax  
  
```  
  
      virtual BOOL ProcessMessageFilter(  
   int code,  
   LPMSG lpMsg   
);  
```  
  
#### Parameters  
 `code`  
 Specifies a hook code. This member function uses the code to determine how to process `lpMsg.`  
  
 `lpMsg`  
 A pointer to a Windows [MSG](../vs140/MSG-Structure.md) structure.  
  
## Return Value  
 Nonzero if the message is processed; otherwise 0.  
  
## Remarks  
 A hook function processes events before they are sent to the application's normal message processing.  
  
 If you override this advanced feature, be sure to call the base-class version to maintain the framework's hook processing.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MessageProc](http://msdn.microsoft.com/library/windows/desktop/ms644987)   
 [About Hooks](http://msdn.microsoft.com/library/windows/desktop/ms644959)