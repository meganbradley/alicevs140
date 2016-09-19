---
title: "CDHtmlDialog::DDX_DHtml_AxControl"
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
ms.assetid: 1f50a5cb-3bfb-4072-8270-b7607aae298c
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::DDX_DHtml_AxControl
Exchanges data between a member variable and the property value of an ActiveX control on an HTML page.  
  
## Syntax  
  
```  
  
      void DDX_DHtml_AxControl(  
   CDataExchange* pDX,  
   LPCTSTR szId,  
   DISPID dispid,  
   VARIANT& var   
);  
void DDX_DHtml_AxControl(  
   CDataExchange* pDX,  
   LPCTSTR szId,  
   LPCTSTR szPropName,  
   VARIANT& var   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object.  
  
 `szId`  
 The value of the object tag's ID parameter in the HTML source for the ActiveX control.  
  
 `dispid`  
 The dispatch ID of the property with which you want to exchange data.  
  
 `szPropName`  
 The name of the property.  
  
 `var`  
 The data member, of type `VARIANT`, [COleVariant](../vs140/COleVariant-Class.md), or [CComVariant](../vs140/CComVariant-Class.md), that holds the value exchanged with the ActiveX control property.  
  
## Example  
 [!CODE [NVC_MFCHtmlHttp#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHttp#1)]  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)