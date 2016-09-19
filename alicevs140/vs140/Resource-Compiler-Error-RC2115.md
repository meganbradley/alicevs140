---
title: "Resource Compiler Error RC2115"
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
ms.assetid: 1b90feb0-f1fb-4f3c-8a9a-c44f9f8dc366
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Compiler Error RC2115
text string or ordinal expected in control  
  
 The *text* field of a CONTROL statement in the **DIALOG** statement must be either a text string or an ordinal reference to the type of control. If using an ordinal, make sure that you have a `#define` statement for the control.