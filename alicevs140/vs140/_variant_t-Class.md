---
title: "_variant_t Class"
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
ms.topic: language-reference
ms.assetid: 6a3cbd4e-0ae8-425e-b4cf-ca0df894c93f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _variant_t Class
**Microsoft Specific**  
  
 A `_variant_t` object encapsulates the `VARIANT` data type. The class manages resource allocation and deallocation and makes function calls to **VariantInit** and **VariantClear** as appropriate.  
  
### Construction  
  
|||  
|-|-|  
|[_variant_t](../vs140/_variant_t--_variant_t.md)|Constructs a `_variant_t` object.|  
  
### Operations  
  
|||  
|-|-|  
|[Attach](../vs140/_variant_t--Attach.md)|Attaches a **VARIANT** object into the `_variant_t` object.|  
|[Clear](../vs140/_variant_t--Clear.md)|Clears the encapsulated **VARIANT** object.|  
|[ChangeType](../vs140/_variant_t--ChangeType.md)|Changes the type of the `_variant_t` object to the indicated **VARTYPE**.|  
|[Detach](../vs140/_variant_t--Detach.md)|Detaches the encapsulated **VARIANT** object from this `_variant_t` object.|  
|[SetString](../vs140/_variant_t--SetString.md)|Assigns a string to this `_variant_t` object.|  
  
### Operators  
  
|||  
|-|-|  
|[Operator =](../vs140/_variant_t--operator-=.md)|Assigns a new value to an existing `_variant_t` object.|  
|[operator ==, !=](../vs140/_variant_t-Relational-Operators.md)|Compare two `_variant_t` objects for equality or inequality.|  
|[Extractors](../vs140/_variant_t-Extractors.md)|Extract data from the encapsulated **VARIANT** object.|  
  
## END Microsoft Specific  
  
## Requirements  
 **Header:** comutil.h  
  
 **Lib:** comsuppw.lib or comsuppwd.lib (see [/Zc:wchar_t (wchar_t Is Native Type)](../Topic/-Zc:wchar_t%20\(wchar_t%20Is%20Native%20Type\).md) for more information)  
  
## See Also  
 [Compiler COM Support Classes](../vs140/Compiler-COM-Support-Classes.md)