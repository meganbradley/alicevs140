---
title: "CDHtmlDialog::DDX_DHtml_CheckBox"
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
ms.assetid: 51081bea-5d5e-49e5-89c3-af47cec17664
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::DDX_DHtml_CheckBox
Exchanges data between a member variable and a check box on an HTML page.  
  
## Syntax  
  
```  
  
      void DDX_DHtml_CheckBox(  
   CDataExchange* pDX,  
   LPCTSTR szId,  
   int& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object.  
  
 `szId`  
 The value that you specified for the HTML control's ID parameter.  
  
 *value*  
 The value being exchanged.  
  
## Example  
 [!CODE [NVC_MFCHtmlHttp#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHttp#2)]  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)