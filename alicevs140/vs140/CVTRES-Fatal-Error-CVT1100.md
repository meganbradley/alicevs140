---
title: "CVTRES Fatal Error CVT1100"
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
ms.assetid: 886e88dd-5818-4b5f-84f2-d2a3d75f0aaf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVTRES Fatal Error CVT1100
duplicate resource — type:type, name:name, language:language, flags:flags, size:size  
  
 The given resource was specified more than once.  
  
 You can get this error if the linker is creating a type library and you did not specify [/TLBID](../Topic/-TLBID%20\(Specify%20Resource%20ID%20for%20TypeLib\).md) and a resource in your project already uses 1. In this case, specify /TLBID and specify another number up to 65535.