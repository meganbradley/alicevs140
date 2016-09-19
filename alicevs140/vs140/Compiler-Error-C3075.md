---
title: "Compiler Error C3075"
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
ms.assetid: f431daa9-e0fa-48f0-a5c3-f99be96b55e3
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3075
'instance' : you cannot embed an instance of a reference type, 'type', in a value-type  
  
 A value type cannot contain an instance of a reference type.  
  
 For more information, see [Automatic Storage for Reference Types](../vs140/C---Stack-Semantics-for-Reference-Types.md).  
  
## Example  
 The following sample generates C3075.  
  
```  
// C3075.cpp  
// compile with: /clr /c  
ref struct U {};  
value struct X {  
   U y;   // C3075  
};  
  
ref struct Y {  
   U y;   // OK  
};  
```