---
title: "DEVMODE and TEXTMETRIC String Conversion Macros"
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
ms.assetid: 85cebec0-2a18-48e5-9c1c-99d5b7f15425
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DEVMODE and TEXTMETRIC String Conversion Macros
These macros create a copy of a [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) or [TEXTMETRIC](http://msdn.microsoft.com/library/windows/desktop/dd145132) structure and convert the strings within the new structure to a new string type. The macros allocate memory on the stack for the new structure and return a pointer to the new structure.  
  
## Syntax  
  
```  
  
      MACRONAME(   
   address_of_structure    
)  
```  
  
## Remarks  
 For example:  
  
 [!CODE [NVC_ATL_Utilities#128](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#128)]  
  
 and:  
  
 [!CODE [NVC_ATL_Utilities#129](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#129)]  
  
 In the macro names, the string type in the source structure is on the left (for example, **A**) and the string type in the destination structure is on the right (for example, **W**). **A** stands for **LPSTR**, **OLE** stands for `LPOLESTR`, **T** stands for `LPTSTR`, and **W** stands for `LPWSTR`.  
  
 Thus, `DEVMODEA2W` copies a `DEVMODE` structure with **LPSTR** strings into a `DEVMODE` structure with `LPWSTR` strings, `TEXTMETRICOLE2T` copies a `TEXTMETRIC` structure with `LPOLESTR` strings into a `TEXTMETRIC` structure with `LPTSTR` strings, and so on.  
  
 The two strings converted in the `DEVMODE` structure are the device name (**dmDeviceName**) and the form name (**dmFormName**). The `DEVMODE` string conversion macros also update the structure size (**dmSize**).  
  
 The four strings converted in the `TEXTMETRIC` structure are the first character (**tmFirstChar**), the last character (**tmLastChar**), the default character (**tmDefaultChar**), and the break character (**tmBreakChar**).  
  
 The behavior of the `DEVMODE` and `TEXTMETRIC` string conversion macros depends on the compiler directive in effect, if any. If the source and destination types are the same, no conversion takes place. Compiler directives change **T** and **OLE** as follows:  
  
|Compiler directive in effect|T becomes|OLE becomes|  
|----------------------------------|---------------|-----------------|  
|none|**A**|**W**|  
|**_UNICODE**|**W**|**W**|  
|**OLE2ANSI**|**A**|**A**|  
|**_UNICODE** and **OLE2ANSI**|**W**|**A**|  
  
 The following table lists the `DEVMODE` and `TEXTMETRIC` string conversion macros.  
  
### DEVMODE and TEXTMETRIC String Conversion Macros  
  
|||  
|-|-|  
|`DEVMODEA2W`|`TEXTMETRICA2W`|  
|`DEVMODEOLE2T`|`TEXTMETRICOLE2T`|  
|`DEVMODET2OLE`|`TEXTMETRICT2OLE`|  
|`DEVMODEW2A`|`TEXTMETRICW2A`|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)   
 [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md)