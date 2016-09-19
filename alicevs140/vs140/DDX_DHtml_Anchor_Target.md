---
title: "DDX_DHtml_Anchor_Target"
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
ms.assetid: 7ce9fc3d-bd62-434b-8cc9-8425e1d670b0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_DHtml_Anchor_Target
Sets or retrieves the target window or frame.  
  
## Syntax  
  
```  
  
      DDX_DHtml_Anchor_Target(  
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
 This macro calls the [CDHtmlDialog::DDX_DHtml_ElementText](../vs140/CDHtmlDialog--DDX_DHtml_ElementText.md) function using the DISPID_IHTMLANCHORELEMENT_TARGET dispatch ID.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [DDX_DHtml Helper Macros](../vs140/DDX_DHtml-Helper-Macros.md)   
 [target Property (IHTMLAnchorElement)](https://msdn.microsoft.com/en-us/library/aa741854.aspx)