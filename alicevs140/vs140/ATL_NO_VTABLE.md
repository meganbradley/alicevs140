---
title: "ATL_NO_VTABLE"
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
ms.assetid: 8b85286c-9ea0-49ca-9b00-5175ac0ea0a9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL_NO_VTABLE
A symbol that prevents the vtable pointer from being initialized in the class's constructor and destructor.  
  
## Syntax  
  
```  
  
ATL_NO_VTABLE  
  
```  
  
## Remarks  
 If the vtable pointer is prevented from being initialized in the class's constructor and destructor, the linker can eliminate the vtable and all of the functions to which it points. Expands to **__declspec(novtable)**.  
  
## Example  
 [!CODE [NVC_ATL_COM#53](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#53)]  
  
## Requirements  
 **Header:** atldef.h  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [Specifying Compiler Optimization for an ATL Project](../vs140/Specifying-Compiler-Optimization-for-an-ATL-Project.md)