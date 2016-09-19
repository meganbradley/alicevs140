---
title: "Compiler Error C2307"
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
ms.assetid: ce6c8033-a673-4679-9883-bedec36ae385
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2307
pragma 'pragma' must be outside function if incremental compilation is enabled  
  
 You must place the `data_seg` pragma between functions if you're using incremental compilation.