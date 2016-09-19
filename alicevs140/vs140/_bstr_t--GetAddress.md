---
title: "_bstr_t::GetAddress"
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
ms.assetid: 09bc9180-867e-4ee5-b22a-8339dc663142
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _bstr_t::GetAddress
**Microsoft Specific**  
  
 Frees any existing string and returns the address of a newly allocated string.  
  
## Syntax  
  
```  
  
BSTR* GetAddress( );  
  
```  
  
## Return Value  
 A pointer to the `BSTR` wrapped by the `_bstr_t`.  
  
## Remarks  
 `GetAddress` affects all `_bstr_t` objects that share a `BSTR`. More than one `_bstr_t` can share a `BSTR` through the use of the copy constructor and and `operator=`.  
  
## Example  
 See [_bstr_t::Assign](../vs140/_bstr_t--Assign.md) for a example using `GetAddress`.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_bstr_t Class](../vs140/_bstr_t-Class.md)