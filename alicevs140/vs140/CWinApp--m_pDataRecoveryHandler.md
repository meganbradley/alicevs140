---
title: "CWinApp::m_pDataRecoveryHandler"
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
ms.assetid: a52d6c8e-59cd-46c7-bce9-51b8a2e77713
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pDataRecoveryHandler
Pointer to the data recovery handler for the application.  
  
## Syntax  
  
```  
CDataRecoveryHandler* m_pDataRecoveryHandler;  
```  
  
## Remarks  
 The data recovery handler of an application monitors open documents and autosaves them. The framework uses the data recovery handler to restore autosaved files when an application restarts after it exits unexpectedly. For more information, see [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)