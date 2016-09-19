---
title: "_ATL_CSTRING_EXPLICIT_CONSTRUCTORS"
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
ms.assetid: 18c344b4-81ea-4977-8e25-e35467286dee
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_CSTRING_EXPLICIT_CONSTRUCTORS
Makes certain `CString` constructors explicit, preventing any unintentional conversions.  
  
## Syntax  
  
```  
  
_ATL_CSTRING_EXPLICIT_CONSTRUCTORS  
  
```  
  
## Remarks  
 When this is defined, all CString constructors that take a single parameter are compiled with the explicit keyword, which prevents implicit conversions of input arguments. This means for example, that when _UNICODE is defined, if you attempt use a char* string as a CString constructor argument, a compiler error will result. Use this macro in situations where you need to prevent implicit conversions between narrow and wide string types.  
  
 By using the _T macro on all constructor string arguments, you can define _ATL_CSTRING_EXPLICIT_CONSTRUCTORS and avoid compile errors regardless of whether _UNICODE is defined.  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [CStringT Class](../vs140/CStringT-Class.md)