---
title: "CDHtmlDialog::GetElementHtml"
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
ms.assetid: e85a04fa-44aa-4ae7-8b01-5effbbc182a6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetElementHtml
Retrieves the **innerHTML** property of the HTML element identified by `szElementId`.  
  
## Syntax  
  
```  
  
      BSTR GetElementHtml(  
   LPCTSTR szElementId   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
## Return Value  
 The **innerHTML** property of the HTML element identified by `szElementId` or **NULL** if the element could not be found.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetElementText](../vs140/CDHtmlDialog--GetElementText.md)   
 [CDHtmlDialog::GetElementProperty](../vs140/CDHtmlDialog--GetElementProperty.md)