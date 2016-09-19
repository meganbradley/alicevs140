---
title: "CHtmlView::OnNavigateComplete2"
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
ms.assetid: bbb05051-1c88-41e0-ab46-bd7e04ad0dd3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnNavigateComplete2
This member function is called by the framework after a navigation to a hyperlink completes (on either a window or frameset element).  
  
## Syntax  
  
```  
  
      virtual void OnNavigateComplete2(  
   LPCTSTR strURL   
);  
```  
  
#### Parameters  
 *strURL*  
 A string expression that evaluates to the URL, UNC file name, or PIDL (a pointer to an item identifier list) that was navigated to.  
  
## Remarks  
 The URL parameter can be a PIDL in the case of a shell name space entity for which there is no URL representation.  
  
 Note that the URL contained in *strURL* can be different from the URL that the browser was told to navigate to, because this URL is the canonicalized and qualified URL. For example, if an application specifies a URL of "www.microsoft.com" in a call to [Navigate](../vs140/CHtmlView--Navigate.md) or [Navigate2](../vs140/CHtmlView--Navigate2.md), the URL passed by `OnNavigateComplete2` will be "http://www.microsoft.com/". Also, if the server has redirected the browser to a different URL, the redirected URL will be reflected here.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DWebBrowserEvents2::NavigateComplete2](https://msdn.microsoft.com/en-us/library/aa768285.aspx)