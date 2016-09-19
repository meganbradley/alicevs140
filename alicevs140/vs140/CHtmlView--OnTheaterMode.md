---
title: "CHtmlView::OnTheaterMode"
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
ms.assetid: 53db102a-c8f2-4e2a-82fc-31f0926a8427
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnTheaterMode
This member function is called by the framework when the [TheaterMode](https://msdn.microsoft.com/en-us/library/aa768273.aspx) property has changed.  
  
## Syntax  
  
```  
  
      virtual void OnTheaterMode(  
   BOOL bTheaterMode   
);  
```  
  
#### Parameters  
 *bTheaterMode*  
 Nonzero if Internet Explorer is in theater mode; zero otherwise.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetTheaterMode](../vs140/CHtmlView--GetTheaterMode.md)   
 [CHtmlView::SetTheaterMode](../vs140/CHtmlView--SetTheaterMode.md)   
 [DWebBrowserEvents2::OnTheaterMode](https://msdn.microsoft.com/en-us/library/aa768292.aspx)