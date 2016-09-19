---
title: "Compiler Error CS0061"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8dfc57a9-653d-4902-a88c-92032ba64024
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0061
Inconsistent accessibility: base interface 'interface 1' is less accessible than interface 'interface 2'  
  
 A [public](../vs140/public--C#-Reference-.md) construct must return a publicly accessible object.  
  
 Interface accessibility cannot be narrowed in a derived interface. For more information, see [Interfaces (C# Programmer's Reference)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md) and [Access Modifiers (C# Programmer's Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0061.  
  
```  
// CS0061.cs  
// compile with: /target:library  
internal interface A {}  
public interface AA : A {}  // CS0061  
  
// OK  
public interface B {}  
internal interface BB : B {}  
  
internal interface C {}  
internal interface CC : C {}  
```