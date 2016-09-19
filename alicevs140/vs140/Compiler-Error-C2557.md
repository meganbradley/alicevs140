---
title: "Compiler Error C2557"
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
ms.assetid: 48a33d82-aa16-4658-b346-2311fcb39864
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2557
'identifier' : private and protected members cannot be initialized without a constructor  
  
 Only members and friends can assign a value to a private or protected member. Nonpublic members should be initialized in the class constructor.