---
title: "Compiler Error C3050"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee090a0b-29cc-4215-a2f9-d82af79b8e82
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3050
'type1' : a ref class cannot inherit from 'type1'  
  
 `System::ValueType` cannot be a base class for a reference type.  
  
 The following sample generates C3050:  
  
```  
// C3050.cpp  
// compile with: /clr /LD  
ref struct X : System::ValueType {};   // C3050  
ref struct Y {};   // OK  
```