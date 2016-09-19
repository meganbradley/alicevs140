---
title: "Linker Tools Warning LNK4010"
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
ms.assetid: 2824cf99-4174-4b60-a6e2-c01e9f1ee52d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4010
invalid subsystem version number number; default subsystem version assumed  
  
 You can specify a version for the image's subsystem ([/SUBSYSTEM](../Topic/-SUBSYSTEM%20\(Specify%20Subsystem\).md)). Each subsystem has a minimum version requirement. If the specified version is lower than the minimum, this warning will occur and the linker will just use the default subsystem.