---
title: "BSCMAKE Error BK1517"
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
ms.assetid: 24391f42-0a3e-40a9-9991-c8b9a6a7b1c7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BSCMAKE Error BK1517
source file for sbrfile compiled with both /Yc and /Yu  
  
 The .sbr file refers to itself. It was probably recompiled with /Yu after compiling with /Yc. Reset the compiler option for the source file to /Yc, then select **Rebuild** to generate new .sbr files. Do not recompile the source file with /Yu.