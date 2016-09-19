---
title: "Compiler Error C3554"
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
ms.assetid: aede18d5-fefc-4da9-9b69-adfe90bfa742
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3554
'decltype' cannot be combined with any other type-specifier  
  
 You cannot qualify the `decltype()` keyword with any type specifier. For example, the following code fragment yields error C3554.  
  
```  
int x;  
unsigned decltype(x); // C3554  
```