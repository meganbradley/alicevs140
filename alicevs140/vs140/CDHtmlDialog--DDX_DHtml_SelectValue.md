---
title: "CDHtmlDialog::DDX_DHtml_SelectValue"
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
ms.assetid: 232dcd11-b497-4833-bd1b-deec5d0768f3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::DDX_DHtml_SelectValue
Gets or sets the value of a list box entry (based on the current index) on an HTML page.  
  
## Syntax  
  
```  
  
      void DDX_DHtml_SelectValue(  
   CDataExchange* pDX,  
   LPCTSTR szId,  
   CString& value   
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
 [!CODE [NVC_MFCHtmlHttp#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHttp#3)]  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)