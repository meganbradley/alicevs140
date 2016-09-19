---
title: "CDHtmlDialog::SetElementText"
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
ms.assetid: fa03828d-5981-4fe7-87b5-7930ecc59ce1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::SetElementText
Sets the **innerText** property of an HTML element.  
  
## Syntax  
  
```  
  
      void SetElementText(  
   LPCTSTR szElementId,  
   BSTR bstrText   
);  
void SetElementText(  
   IUnknown *punkElem,  
   BSTR bstrText   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
 `bstrText`  
 The new value of the **innerText** property.  
  
 `punkElem`  
 The **IUnknown** pointer of an HTML element.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::SetElementHtml](../vs140/CDHtmlDialog--SetElementHtml.md)   
 [CDHtmlDialog::SetElementProperty](../vs140/CDHtmlDialog--SetElementProperty.md)