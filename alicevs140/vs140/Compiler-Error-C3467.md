---
title: "Compiler Error C3467"
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
ms.assetid: e2b844d0-4920-412f-99fd-cd8051c4aa41
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3467
'type' : this type has already been forwarded  
  
 The compiler found more than one forward type declaration for the same type. Only one declaration per type is allowed.  
  
 For more information, see [Type Forwarding](../vs140/Type-Forwarding--C---CLI-.md).  
  
## Example  
 The following sample creates a component.  
  
```  
// C3467.cpp  
// compile with: /LD /clr  
public ref class R {};  
```  
  
## Example  
 The following sample generates C3467.  
  
```  
// C3467_b.cpp  
// compile with: /clr /c  
#using "C3467.dll"  
[ assembly:TypeForwardedTo(R::typeid) ];  
[ assembly:TypeForwardedTo(R::typeid) ];   // C3467  
```