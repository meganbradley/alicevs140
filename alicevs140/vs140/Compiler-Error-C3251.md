---
title: "Compiler Error C3251"
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
ms.assetid: 541c163e-5ee9-457c-a1e5-da860788b10d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3251
cannot invoke base class method on a value type instance  
  
 The following error occurs because `GetClass` is a member of `Microsoft.Runtime.Object`, not of `Microsoft.Runtime.Integer4`.