---
title: "_ATL_SECURE_NO_WARNINGS"
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
ms.assetid: 587d29d8-a75a-44a3-bec8-f724087e5e73
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_SECURE_NO_WARNINGS
Suppresses compiler warnings for the use of deprecated ATL functions.  
  
## Syntax  
  
```  
#define _ATL_SECURE_NO_WARNINGS  
```  
  
## Example  
 This code sample would cause a compiler warning if _ATL_SECURE_NO_WARNINGS were not defined.  
  
 [!CODE [NVC_ATL_Utilities#125](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#125)]  
  
 [!CODE [NVC_ATL_Utilities#126](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#126)]  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)