---
title: "CWinApp::GetDataRecoveryHandler"
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
ms.assetid: e011b4f9-4a2f-4a43-b5e0-54e876a54ee0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetDataRecoveryHandler
Gets the data recovery handler for this instance of the application.  
  
## Syntax  
  
```  
virtual CDataRecoveryHandler *GetDataRecoveryHandler();  
```  
  
## Return Value  
 The data recovery handler for this instance of the application.  
  
## Remarks  
 Each application that uses the restart manager must have one instance of the [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md). This class is responsible for monitoring open documents and autosaving files. The behavior of the `CDataRecoveryHandler` depends on the configuration of the restart manager. For more information, see [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md).  
  
 This method returns `NULL` on operating systems earlier than [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]. The restart manager is not supported on operating systems earlier than [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)].  
  
 If the application does not currently have a data recovery handler, this method creates one and returns a pointer to it.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)