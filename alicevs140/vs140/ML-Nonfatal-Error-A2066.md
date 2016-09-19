---
title: "ML Nonfatal Error A2066"
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
ms.topic: article
ms.assetid: 58220fdf-fb8f-47fc-a36d-737867361185
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Nonfatal Error A2066
**incompatible CPU mode and segment size**  
  
 An attempt was made to open a segment with a **USE16**, **USE32**, or **FLAT** attribute that was not compatible with the specified CPU, or to change to a 16-bit CPU while in a 32-bit segment.  
  
 The **USE32** and **FLAT** attributes must be preceded by the .386 or greater processor directive.  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)