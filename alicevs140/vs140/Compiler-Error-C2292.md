---
title: "Compiler Error C2292"
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
ms.assetid: 256b392f-2b8f-4162-b578-e7633984e162
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2292
'identifier': best case inheritance representation: 'representation1' declared but 'representation2' required  
  
 Compiling the following code with [/vmb](../vs140/-vmb---vmg--Representation-Method-.md) ("Best-case always" representation) causes C2292.  
  
```  
// C2292.cpp  
// compile with: /vmb  
class __single_inheritance X;  
  
struct A { };  
struct B { };  
struct X : A, B { };  // C2292, X uses multiple inheritance  
```