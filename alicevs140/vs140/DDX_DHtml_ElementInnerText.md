---
title: "DDX_DHtml_ElementInnerText"
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
ms.assetid: 39099190-6c6d-4108-b470-5cacff44c76e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_DHtml_ElementInnerText
Sets or retrieves the text between the start and end tags of the current element.  
  
## Syntax  
  
```  
  
      DDX_DHtml_ElementInnerText(  
   CDataExchange* dx,  
   LPCTSTR name,  
   CString& var   
)  
```  
  
#### Parameters  
 `dx`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object.  
  
 *name*  
 The value that you specified for the HTML control's ID parameter.  
  
 `var`  
 The value being exchanged.  
  
## Remarks  
 This macro calls the [CDHtmlDialog::DDX_DHtml_ElementText](../vs140/CDHtmlDialog--DDX_DHtml_ElementText.md) function using the DISPID_IHTMLELEMENT_INNERTEXT dispatch ID.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [DDX_DHtml Helper Macros](../vs140/DDX_DHtml-Helper-Macros.md)   
 [innerText Property (IHTMLElement)](http://msdn.microsoft.com/library/aa752299)