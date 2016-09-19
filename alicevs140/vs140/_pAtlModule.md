---
title: "_pAtlModule"
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
ms.assetid: 0ecde3a9-3f4d-4c7b-bb54-713ce05c4777
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _pAtlModule
A global variable storing a pointer to the current module.  
  
## Syntax  
  
```  
__declspec(selectany) CAtlModule * _pAtlModule  
```  
  
## Remarks  
 Methods on this global variable can be used to provide the functionality that the (now obsolete) class [CComModule](../vs140/CComModule-Class.md) provided in Visual C++ 6.0.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#97](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#97)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Global Variables](../vs140/ATL-Global-Variables.md)