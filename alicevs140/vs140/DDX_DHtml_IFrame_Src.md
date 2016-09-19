---
title: "DDX_DHtml_IFrame_Src"
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
ms.assetid: 825c5516-0e5d-4490-be0d-547b93045933
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_DHtml_IFrame_Src
Sets or retrieves the URL of the associated frame.  
  
## Syntax  
  
```  
  
      DDX_DHtml_IFrame_Src(  
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
 This macro calls the [CDHtmlDialog::DDX_DHtml_ElementText](../vs140/CDHtmlDialog--DDX_DHtml_ElementText.md) function using the DISPID_IHTMLFRAMEBASE_SRC dispatch ID.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [DDX_DHtml Helper Macros](../vs140/DDX_DHtml-Helper-Macros.md)   
 [src Property (IHTMLFrameBase)](https://msdn.microsoft.com/en-us/library/aa752423.aspx)