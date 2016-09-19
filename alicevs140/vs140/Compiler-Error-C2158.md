---
title: "Compiler Error C2158"
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
ms.assetid: 39028899-e95c-4809-8e65-6111118641ee
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2158
'type' : #pragma make_public directive is currently supported for native non-template types only  
  
 The [make_public](../vs140/make_public.md) pragma can only be applied to a native, non-template type.  
  
## Example  
 The following sample generates C2158.  
  
```  
// C2158.cpp  
// compile with: /clr /c  
ref class A {};  
#pragma make_public(A)   // C2158  
  
template< typename T >  
class B {};  
#pragma make_public(B)   // C2158  
#pragma make_public(B<int>)   // C2158  
  
void C () {}  
#pragma make_public(C)   // C2158  
  
class D {};  
#pragma make_public(D)   // OK  
```