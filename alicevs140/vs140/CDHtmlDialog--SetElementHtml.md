---
title: "CDHtmlDialog::SetElementHtml"
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
ms.assetid: cc787e5e-debc-4161-b5fa-272a66065aaf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::SetElementHtml
Sets the **innerHTML** property of an HTML element.  
  
## Syntax  
  
```  
  
      void SetElementHtml(  
   LPCTSTR szElementId,  
   BSTR bstrText   
);  
void SetElementHtml(  
   IUnknown *punkElem,  
   BSTR bstrText   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
 `bstrText`  
 The new value of the **innerHTML** property.  
  
 `punkElem`  
 The **IUnknown** pointer of an HTML element.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::SetElementText](../vs140/CDHtmlDialog--SetElementText.md)   
 [CDHtmlDialog::SetElementProperty](../vs140/CDHtmlDialog--SetElementProperty.md)