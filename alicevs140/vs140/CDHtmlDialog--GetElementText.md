---
title: "CDHtmlDialog::GetElementText"
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
ms.assetid: 74783d22-0aa4-4096-9c8b-4cd29f59b10c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetElementText
Retrieves the **innerText** property of the HTML element identified by `szElementId`.  
  
## Syntax  
  
```  
  
      BSTR GetElementText(  
   LPCTSTR szElementId   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
## Return Value  
 The **innerText** property of the HTML element identified by `szElementId` or **NULL** if the property or element could not be found.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetElementHtml](../vs140/CDHtmlDialog--GetElementHtml.md)   
 [CDHtmlDialog::GetElementProperty](../vs140/CDHtmlDialog--GetElementProperty.md)