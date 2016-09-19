---
title: "CHtmlView::Refresh2"
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
ms.assetid: 8e0b6237-da65-47e2-bf51-37115aa0ea79
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::Refresh2
Reloads the file that Internet Explorer is currently displaying.  
  
## Syntax  
  
```  
  
      void Refresh2(  
   int nLevel   
);  
```  
  
#### Parameters  
 `nLevel`  
 The address of the variable specifying the refresh level. The possible variables are defined in [RefreshConstants](https://msdn.microsoft.com/en-us/library/aa768363.aspx), in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 Unlike [Refresh](../vs140/CHtmlView--Refresh.md), `Refresh2` contains a parameter that specifies the refresh level.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IWebBrowser2::Refresh2](https://msdn.microsoft.com/en-us/library/aa768260.aspx)