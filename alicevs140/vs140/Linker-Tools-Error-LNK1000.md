---
title: "Linker Tools Error LNK1000"
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
ms.assetid: 86421b9a-460a-4285-8dce-9b8257d78122
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1000
unknown error; consult documentation for technical support options  
  
 Note the circumstances of the error, try to isolate the problem and create a reproducible test case, then contact `Microsoft Product Support Services`. For information on how to investigate and report these errors, see [http://support.microsoft.com/default.aspx?scid=kb;en-us;134650](http://support.microsoft.com/default.aspx?scid=kb;en-us;134650).  
  
 You may get this error if you mix standard header files (for example, dos.h) and your own files. `#include` the standard headers first, followed by your own header files.