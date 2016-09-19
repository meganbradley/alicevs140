---
title: "NMAKE Fatal Error U1087"
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
ms.assetid: 5236ab54-e117-484d-99c3-852b061fd3d0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1087
cannot have : and :: dependents for same target  
  
 A target cannot be specified in both a single-colon (**:**) and a double-colon (`::`) dependency.  
  
 To specify a target in multiple description blocks, use `::` in each dependency line.