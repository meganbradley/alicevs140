---
title: "Compiler Error C3753"
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
ms.assetid: a5b99e28-796c-4107-a673-97c2ae3bb2b9
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3753
a generic property is not allowed  
  
 Generic parameter lists can only appear on managed classes, structs, or functions.  
  
 For more information, see [Generics (C++)](../vs140/Generics---C---Component-Extensions-.md) and [property](../vs140/property---C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C3753.  
  
```  
// C3753.cpp  
// compile with: /clr /c  
ref struct A {  
   generic <typename T>  
   property int i;   // C3753 error  
};  
```