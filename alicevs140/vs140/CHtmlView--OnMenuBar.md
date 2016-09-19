---
title: "CHtmlView::OnMenuBar"
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
ms.assetid: c5e8afcd-b868-4441-9b68-123c7a507698
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnMenuBar
This member function is called by the framework when the [MenuBar](https://msdn.microsoft.com/en-us/library/aa752131.aspx) property has changed.  
  
## Syntax  
  
```  
  
      virtual void OnMenuBar(  
   BOOL bMenuBar   
);  
```  
  
#### Parameters  
 *bMenuBar*  
 Nonzero if the Internet Explorer menu bar is visible; zero otherwise.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetMenuBar](../vs140/CHtmlView--GetMenuBar.md)   
 [CHtmlView::SetMenuBar](../vs140/CHtmlView--SetMenuBar.md)   
 [DWebBrowserEvents2::OnMenuBar](https://msdn.microsoft.com/en-us/library/aa768290.aspx)