---
title: "CDHtmlDialog::DDX_DHtml_SelectIndex"
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
ms.assetid: af2d1e55-0f76-4e71-969e-a9fd21b206d8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::DDX_DHtml_SelectIndex
Gets or sets the index of a list box on an HTML page.  
  
## Syntax  
  
```  
  
      void DDX_DHtml_SelectIndex(  
   CDataExchange* pDX,  
   LPCTSTR szId,  
   long& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object.  
  
 `szId`  
 The value that you specified for the HTML control's id parameter.  
  
 *value*  
 The value being exchanged.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)