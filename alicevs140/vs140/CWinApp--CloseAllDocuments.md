---
title: "CWinApp::CloseAllDocuments"
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
ms.assetid: dde4acc5-028b-4b21-a08a-f7c5b50ac2b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::CloseAllDocuments
Call this member function to close all open documents before exiting.  
  
## Syntax  
  
```  
  
      void CloseAllDocuments(  
   BOOL bEndSession   
);  
```  
  
#### Parameters  
 `bEndSession`  
 Specifies whether or not the Windows session is being ended. It is **TRUE** if the session is being ended; otherwise **FALSE**.  
  
## Remarks  
 Call [HideApplication](../vs140/CWinApp--HideApplication.md) before calling `CloseAllDocuments`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SaveAllModified](../vs140/CWinApp--SaveAllModified.md)   
 [CWinApp::HideApplication](../vs140/CWinApp--HideApplication.md)