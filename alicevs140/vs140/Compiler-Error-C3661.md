---
title: "Compiler Error C3661"
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
ms.topic: error-reference
ms.assetid: 50793fd1-1829-4b29-ad0d-094ef2068b43
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3661
explicit override list did not find any methods to override  
  
 An explicit override specified one or more type names.  However, there was no function with the necessary signature in the type(s) that matched the overriding function's signature.  If you attempt to override based on type name, there must be one or more virtual functions in the specified type(s) that match the signature of the overriding function.  
  
 For more information, see [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md).