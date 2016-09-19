---
title: "CHtmlView::OnStatusBar"
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
ms.assetid: 670810b6-75fa-4848-80ef-1143e39759ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnStatusBar
This member function is called by the framework when the [StatusBar](https://msdn.microsoft.com/en-us/library/aa768270.aspx) property has changed.  
  
## Syntax  
  
```  
  
      virtual void OnStatusBar(  
   BOOL bStatusBar   
);  
```  
  
#### Parameters  
 *bStatusBar*  
 Nonzero if Internet Explorer's status bar is visible or zero otherwise.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetStatusBar](../vs140/CHtmlView--GetStatusBar.md)   
 [CHtmlView::SetStatusBar](../vs140/CHtmlView--SetStatusBar.md)   
 [DWebBrowserEvents2::OnStatusBar](https://msdn.microsoft.com/en-us/library/aa768291.aspx)