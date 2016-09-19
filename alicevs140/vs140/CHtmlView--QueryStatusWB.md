---
title: "CHtmlView::QueryStatusWB"
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
ms.assetid: 30af8d21-24d5-4340-a1a6-1ea464c9926c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::QueryStatusWB
Call this member function to query a command status.  
  
## Syntax  
  
```  
  
      OLECMDF QueryStatusWB(  
   OLECMDID cmdID   
) const;  
```  
  
#### Parameters  
 `cmdID`  
 The [OLECMDID](http://msdn.microsoft.com/library/windows/desktop/ms691264) value of the command for which the caller needs status information.  
  
## Return Value  
 The address of the [OLECMDF](http://msdn.microsoft.com/library/windows/desktop/ms695237) value that receives the status of the command.  
  
## Remarks  
 `QueryStatusWB` implements the behavior of the [IOleCommandTarget::QueryStatus](http://msdn.microsoft.com/library/windows/desktop/ms688491) method.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::ExecWB](../vs140/CHtmlView--ExecWB.md)   
 [IWebBrowser2::QueryStatusWB](https://msdn.microsoft.com/en-us/library/aa752139.aspx)