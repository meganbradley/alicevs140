---
title: "Linker Tools Error LNK2017"
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
ms.assetid: f7c21733-b0fb-4888-a295-9b453ba6ee77
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK2017
'symbol' relocation to 'segment' invalid without /LARGEADDRESSAWARE:NO  
  
 You are trying to build a 64-bit image with 32-bit addresses. To do this, you must:  
  
-   Use a fixed load address.  
  
-   Restrict the image to 3 GB.  
  
-   Specify [/largeaddressaware:no](../vs140/-LARGEADDRESSAWARE--Handle-Large-Addresses-.md).