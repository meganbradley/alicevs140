---
title: "Linker Tools Warning LNK4022"
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
ms.assetid: 890f487e-db98-45dd-a226-c7ccead82b1e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4022
cannot find unique match for symbol 'symbol'  
  
 LINK or LIB found multiple matches for the given undecorated symbol and it could not resolve the ambiguity. No output file (.exe, .dll, .exp, or .lib) is produced. This warning is followed by one warning [LNK4002](../vs140/Linker-Tools-Warning-LNK4002.md) for each duplicate symbol and is finally followed by fatal error [LNK1152](../vs140/Linker-Tools-Error-LNK1152.md).  
  
 To prevent this warning, specify the symbol in its decorated form. Run [DUMPBIN](../vs140/DUMPBIN-Options.md) on the object to see decorated names.