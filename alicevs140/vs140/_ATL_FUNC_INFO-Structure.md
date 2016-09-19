---
title: "_ATL_FUNC_INFO Structure"
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
ms.topic: article
ms.assetid: 441ebe2c-f971-47de-9f52-a258e8d6f88e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_FUNC_INFO Structure
Contains type information used to describe a method or property on a dispinterface.  
  
## Syntax  
  
```  
  
      struct _ATL_FUNC_INFO{  
   CALLCONV cc;  
   VARTYPE vtReturn;  
   SHORT nParams;  
   VARTYPE pVarTypes[_ATL_MAX_VARTYPES];  
};  
```  
  
## Members  
 **cc**  
 The calling convention. When using this structure with the [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) class, this member must be **CC_STDCALL**. `CC_CDECL` is the only option supported in Windows CE for the `CALLCONV` field of the `_ATL_FUNC_INFO` structure. Any other value is unsupported thus its behavior undefined.  
  
 **vtReturn**  
 The variant type of the function return value.  
  
 **nParams**  
 The number of function parameters.  
  
 **pVarTypes**  
 An array of variant types of the function parameters.  
  
## Remarks  
 Internally, ATL uses this structure to hold information obtained from a type library. You may need to manipulate this structure directly if you provide type information for an event handler used with the [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) class and [SINK_ENTRY_INFO](../vs140/SINK_ENTRY_INFO.md) macro.  
  
## Example  
 Given a dispinterface method defined in IDL:  
  
 [!CODE [NVC_ATL_Windowing#139](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#139)]  
  
 you would define an `_ATL_FUNC_INFO` structure:  
  
 [!CODE [NVC_ATL_Windowing#140](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#140)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Structures](../vs140/ATL-Structures.md)   
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)   
 [SINK_ENTRY_INFO](../vs140/SINK_ENTRY_INFO.md)