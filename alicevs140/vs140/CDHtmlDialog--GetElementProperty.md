---
title: "CDHtmlDialog::GetElementProperty"
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
ms.assetid: 7d9d900e-62a7-4670-bc22-c1dfc1de366e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetElementProperty
Retrieves the value of the property identified by `dispid` from the HTML element identified by `szElementId`.  
  
## Syntax  
  
```  
  
      VARIANT GetElementProperty(  
   LPCTSTR szElementId,  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
 `dispid`  
 The dispatch ID of a property.  
  
## Return Value  
 The value of the property or an empty variant if the property or element could not be found.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetElementHtml](../vs140/CDHtmlDialog--GetElementHtml.md)   
 [CDHtmlDialog::GetElementText](../vs140/CDHtmlDialog--GetElementText.md)