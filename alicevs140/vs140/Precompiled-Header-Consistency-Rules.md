---
title: "Precompiled Header Consistency Rules"
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
ms.topic: article
ms.assetid: 844b1a14-5b0b-4276-a1f5-cc62f13f6dda
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Precompiled Header Consistency Rules
This section discusses guidelines that will help you use precompiled headers more efficiently:  
  
-   [Consistency Rules for Per-File Use of Precompiled Headers](../vs140/Consistency-Rules-for-Per-File-Use-of-Precompiled-Headers.md)  
  
-   [Consistency Rules for /Yc and /Yu](../vs140/Consistency-Rules-for--Yc-and--Yu.md)  
  
 Because PCH files contain information about the machine environment as well as memory address information about the program, you should only use a PCH file on the machine where it was created.  
  
## See Also  
 [Creating Precompiled Header Files](../vs140/Creating-Precompiled-Header-Files.md)