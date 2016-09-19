---
title: "CHtmlView::ExecWB"
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
ms.assetid: e489f0fc-ece7-4bb1-9510-822f858f20a9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::ExecWB
Call this member function to execute a command in the WebBrowser or Internet Explorer.  
  
## Syntax  
  
```  
  
      void ExecWB(  
   OLECMDID cmdID,  
   OLECMDEXECOPT cmdexecopt,  
   VARIANT* pvaIn,  
   VARIANT* pvaOut   
);  
```  
  
#### Parameters  
 `cmdID`  
 The command to execute.  
  
 *cmdexecopt*  
 The options set for executing the command.  
  
 `pvaIn`  
 A variant used for specifying command input arguments.  
  
 *pvaOut*  
 A variant used for specifying command output arguments.  
  
## Remarks  
 See [IWebBrowser2::ExecWB](https://msdn.microsoft.com/en-us/library/aa752117.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::Stop](../vs140/CHtmlView--Stop.md)