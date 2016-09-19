---
title: "CHtmlView::OnDownloadBegin"
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
ms.assetid: 1ec816d5-337e-4e89-9b8e-d9f7c743e8be
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnDownloadBegin
This member function is called by the framework to begin downloading a document.  
  
## Syntax  
  
```  
  
virtual void OnDownloadBegin( );  
  
```  
  
## Remarks  
 This event is fired shortly after the [OnBeforeNavigate2](../vs140/CHtmlView--OnBeforeNavigate2.md) event, unless the navigation is canceled. Any animation or "busy" indication that the container needs to display should be connected to this event.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::OnDownloadComplete](../vs140/CHtmlView--OnDownloadComplete.md)   
 [CHtmlView::Navigate](../vs140/CHtmlView--Navigate.md)   
 [CHtmlView::Navigate2](../vs140/CHtmlView--Navigate2.md)