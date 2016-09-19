---
title: "Compiler Error C2713"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: bae9bee3-b4b8-4be5-b6a5-02df587a7278
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2713
only one form of exception handling permitted per function  
  
 You cannot use structured exception handling (`__try`/`__except`) and C++ exception handling (`try`/`catch`) in the same function.