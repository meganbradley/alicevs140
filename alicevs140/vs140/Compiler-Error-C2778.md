---
title: "Compiler Error C2778"
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
ms.assetid: b24cb732-2914-42cc-8928-e2d87b393428
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2778
improperly formed GUID in __declspec(uuid())  
  
 An incorrect GUID is supplied to the [uuid](../vs140/uuid--C---.md) extended attribute.  
  
 The GUID must be a string of hexadecimal numbers with the following format:  
  
```  
// C2778a.cpp  
// compile with: /c  
struct __declspec(uuid("00000000-0000-0000-0000-000000000000")) A {};  
struct __declspec(uuid("{00000000-0000-0000-0000-000000000000}")) B{};  
```  
  
 The `uuid` extended attribute accepts strings recognized by [CLSIDFromString](http://msdn.microsoft.com/library/windows/desktop/ms680589), with or without brace delimiters.  
  
 The following sample generates C2778:  
  
```  
// C2778b.cpp  
struct __declspec(uuid(" 00000000-0000-0000-0000-000000000000 ")) C { };   // C2778  
struct __declspec(uuid("00000000000000000000000000000000")) D { };   // C2778  
```