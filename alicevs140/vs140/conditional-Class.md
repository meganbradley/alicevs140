---
title: "conditional Class"
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
ms.assetid: ece9f539-fb28-4e26-a79f-3264bc984493
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# conditional Class
Selects one of two types, depending on the specified condition.  
  
## Syntax  
  
```  
template <bool B, class T1, class T2>  
    struct conditional;  
  
template <bool _Test, class _T1, class _T2>  
    using conditional_t = typename conditional<_Test, _T1, _T2>::type;  
```  
  
#### Parameters  
 `B`  
 The value that determines the selected type.  
  
 `T1`  
 The type result when B is true.  
  
 `T2`  
 The type result when B is false.  
  
## Remarks  
 The template member typedef `conditional<B, T1, T2>::type` evaluates to `T1` when `B` evaluates to `true`, and evaluates to `T2` when `B` evaluates to `false`.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)