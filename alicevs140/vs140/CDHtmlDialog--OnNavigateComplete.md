---
title: "CDHtmlDialog::OnNavigateComplete"
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
ms.assetid: 721fb4ae-46b9-4f36-8607-f69e7ceba955
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::OnNavigateComplete
Called by the framework after navigation to the specified URL is completed.  
  
## Syntax  
  
```  
  
      virtual void OnNavigateComplete(  
   LPDISPATCH pDisp,  
   LPCTSTR szUrl   
);  
```  
  
#### Parameters  
 `pDisp`  
 A pointer to an `IDispatch` object.  
  
 `szUrl`  
 A pointer to a string containing the URL that was navigated to.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::OnDocumentComplete](../vs140/CDHtmlDialog--OnDocumentComplete.md)