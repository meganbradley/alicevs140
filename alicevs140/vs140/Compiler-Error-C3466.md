---
title: "Compiler Error C3466"
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
ms.assetid: 69a877d9-a749-474b-bfc3-8d3fd53ba8fd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3466
'type' : a specialization of a generic class cannot be forwarded  
  
 You cannot use type forwarding on a specialization of a generic class.  
  
 For more information, see [Type Forwarding](../vs140/Type-Forwarding--C---CLI-.md).  
  
## Example  
 The following sample creates a component.  
  
```  
// C3466.cpp  
// compile with: /clr /LD  
generic<typename T>  
public ref class GR {};  
  
public ref class GR2 {};  
```  
  
## Example  
 The following sample generates C3466.  
  
```  
// C3466_b.cpp  
// compile with: /clr /c  
#using "C3466.dll"  
[assembly:TypeForwardedTo(GR<int>::typeid)];   // C3466  
[assembly:TypeForwardedTo(GR2::typeid)];   // OK  
```