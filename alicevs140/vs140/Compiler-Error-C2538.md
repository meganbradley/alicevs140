---
title: "Compiler Error C2538"
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
ms.assetid: af7b97c0-3096-4059-9b05-bf860a18c116
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2538
new : cannot specify initializer for arrays  
  
 An initializer is given for an array created with the `new` operator. The `new` operator creates arrays of objects by calling the default constructor for each element of the array. The elements of the array cannot be initialized to distinct values.