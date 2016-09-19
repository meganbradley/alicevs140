---
title: "CDHtmlDialog::SetElementProperty"
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
ms.assetid: ec05420e-7d85-4f7e-88b0-1c47d754c829
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::SetElementProperty
Sets a property of an HTML element.  
  
## Syntax  
  
```  
  
      void SetElementProperty(  
   LPCTSTR szElementId,  
   DISPID dispid,  
   VARIANT *pVar   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
 `dispid`  
 The dispatch ID of the property to set.  
  
 *pVar*  
 The new value of the property.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::SetControlProperty](../vs140/CDHtmlDialog--SetControlProperty.md)   
 [CDHtmlDialog::SetElementText](../vs140/CDHtmlDialog--SetElementText.md)   
 [CDHtmlDialog::SetElementHtml](../vs140/CDHtmlDialog--SetElementHtml.md)