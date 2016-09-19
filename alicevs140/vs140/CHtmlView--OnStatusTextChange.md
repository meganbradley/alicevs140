---
title: "CHtmlView::OnStatusTextChange"
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
ms.assetid: 91bb251e-c1e0-4a8d-8cc0-c28b919a2b24
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnStatusTextChange
This member function is called by the framework to notify an application that the text of the status bar associated with the WebBrowser control has changed.  
  
## Syntax  
  
```  
  
      virtual void OnStatusTextChange(  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 `lpszText`  
 A string that contains the new status bar text.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)