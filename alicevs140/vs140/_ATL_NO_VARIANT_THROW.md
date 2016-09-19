---
title: "_ATL_NO_VARIANT_THROW"
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
ms.assetid: 04b0fcaa-aceb-475d-a46d-00720adb7d6d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_NO_VARIANT_THROW
Suppresses the [CComVariant Class](../vs140/CComVariant-Class.md) from throwing exceptions.  
  
## Syntax  
  
```  
#define _ATL_NO_VARIANT_THROW  
```  
  
## Remarks  
 Define this macro if your module must not throw exceptions. When this macro is defined, `CComVariant` will not throw exceptions. By default, this macro is not defined.  
  
## See Also  
 [ATL Macros](../vs140/ATL-Macros.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)