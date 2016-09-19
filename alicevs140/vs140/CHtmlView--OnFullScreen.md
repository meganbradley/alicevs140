---
title: "CHtmlView::OnFullScreen"
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
ms.assetid: 737a3d7f-3f71-409b-81a8-fad3abd78c0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnFullScreen
This member function is called by the framework when the [FullScreen](https://msdn.microsoft.com/en-us/library/aa752119.aspx) property has changed.  
  
## Syntax  
  
```  
  
      virtual void OnFullScreen(  
   BOOL bFullScreen   
);  
```  
  
#### Parameters  
 *bFullScreen*  
 Nonzero if Internet Explorer is in full screen mode; zero otherwise.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetFullScreen](../vs140/CHtmlView--GetFullScreen.md)   
 [CHtmlView::SetFullScreen](../vs140/CHtmlView--SetFullScreen.md)   
 [DWebBrowserEvents2::OnFullScreen](https://msdn.microsoft.com/en-us/library/aa768289.aspx)