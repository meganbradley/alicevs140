---
title: "Compiler Error C2518"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: a7895b47-da90-4851-ac97-18e81479595a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2518
keyword 'keyword' illegal in base class list; ignored  
  
 The keywords `class` and `struct` should not appear in a base class list.  
  
 The following sample generates C2518:  
  
```  
// C2518.cpp  
// compile with: /c  
class B {};  
class C : public class B {};   // C2518  
class D: public B {};   // OK  
```