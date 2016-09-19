---
title: "move"
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
ms.assetid: e6d5bd4f-b2fb-4826-9541-018fac5996dd
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# move
Unconditionally casts its argument to an rvalue reference, and thereby signals that it can be moved if its type is move-enabled.  
  
## Syntax  
  
```  
template<class Type>  
    constexpr typename remove_reference<Type>::type&& move(Type&& Arg) noexcept;  
  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Type`|A type deduced from the type of the argument passed in `Arg`, together with the reference collapsing rules.|  
|`Arg`|The argument to cast. Although the type of `Arg` appears to be specified as an rvalue reference, `move` also accepts lvalue arguments because lvalue references can bind to rvalue references.|  
  
## Return Value  
 `Arg` as an rvalue reference, whether or not its type is a reference type.  
  
## Remarks  
 The template argument `Type` is not intended to be specified explicitly, but to be deduced from the type of the value passed in `Arg`. The type of `Type` is further adjusted according to the reference collapsing rules.  
  
 `move` does not move its argument. Instead, by unconditionally casting its argument—which might be an lvalue—to an rvalue reference, it enables the compiler to subsequently move, rather than copy, the value passed in `Arg` if its type is move-enabled. If its type is not move-enabled, it is copied instead.  
  
 If the value passed in `Arg` is an lvalue—that is, it has a name or its address can be taken—it's invalidated when the move occurs. Do not refer to the value passed in `Arg` by its name or address after it's been moved.  
  
## Requirements  
 **Header:** <utility\>  
  
 **Namespace:** std  
  
## See Also  
 [<utility\>](../vs140/-utility-.md)   
 [Lvalues and Rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)