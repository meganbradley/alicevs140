---
title: "Compiler Error C3065"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e7a0bc69-1c68-459e-a7c4-93c65609ff7c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3065
property declaration at non-class scope is not allowed  
  
 The [property](../vs140/property--C---.md) __declspec modifier was used outside a class.  A property can only be declared inside a class.  
  
 The following sample generates C3065:  
  
```  
// C3065.cpp  
// compile with: /c  
__declspec(property(get=get_i)) int i;   // C3065  
  
class x {  
public:  
   __declspec(property(get=get_i)) int i;   // OK  
};  
```