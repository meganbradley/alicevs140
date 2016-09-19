---
title: "NMAKE Warning U4011"
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
ms.assetid: e8244514-eba6-4285-8853-7baeefdcd8a4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Warning U4011
'target' : not all dependents available; target not built  
  
 A dependent of the given target either did not exist or was out-of-date, and a command for updating the dependent returned a nonzero exit code. The /K option told NMAKE to continue processing unrelated parts of the build and to issue an exit code 1 when the NMAKE session is finished.  
  
 This warning is preceded by warning [U4010](../vs140/NMAKE-Warning-U4010.md) for each dependent that failed to be created or updated.