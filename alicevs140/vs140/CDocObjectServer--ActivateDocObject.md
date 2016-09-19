---
title: "CDocObjectServer::ActivateDocObject"
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
ms.assetid: dbeaa1d9-9ca4-481a-84a4-86530be832ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServer::ActivateDocObject
Call this function to activate (but not show) the document object server.  
  
## Syntax  
  
```  
  
void ActivateDocObject( );  
```  
  
## Remarks  
 `ActivateDocObject` calls `IOleDocumentSite`'s **ActivateMe** method, but does not show the view because it waits for specific instructions on how to set up and display the view, given in the call to [CDocObjectServer::OnActivateView](../vs140/CDocObjectServer--OnActivateView.md).  
  
 Together, `ActivateDocObject` and `OnActivateView` activate and display the DocObject view. DocObject activation differs from other kinds of OLE in-place activation. DocObject activation bypasses displaying in-place hatch borders and object adornments (such as sizing handles), ignores object extent functions, and draws scroll bars within the view rectangle as opposed to drawing them outside that rectangle (as in normal in-place activation).  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServerItem Class](../vs140/CDocObjectServerItem-Class.md)