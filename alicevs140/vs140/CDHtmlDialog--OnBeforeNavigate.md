---
title: "CDHtmlDialog::OnBeforeNavigate"
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
ms.assetid: 0a7b27a1-dccf-448b-a559-a098f1a3770d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::OnBeforeNavigate
Called by the framework to cause an event to fire before a navigation occurs.  
  
## Syntax  
  
```  
  
      virtual void OnBeforeNavigate(  
   LPDISPATCH pDisp,  
   LPCTSTR szUrl   
);  
```  
  
#### Parameters  
 `pDisp`  
 A pointer to an `IDispatch` object.  
  
 `szUrl`  
 A pointer to a string containing the URL to navigate to.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::OnNavigateComplete](../vs140/CDHtmlDialog--OnNavigateComplete.md)