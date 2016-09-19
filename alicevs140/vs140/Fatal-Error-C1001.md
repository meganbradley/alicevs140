---
title: "Fatal Error C1001"
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
ms.assetid: 5736cdb3-22c8-4fad-aa85-d5e0d2b232f4
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1001
INTERNAL COMPILER ERROR(compiler file file, line number)  
  
 The compiler cannot generate correct code for a construct, probably due to the combination of an expression and an optimization option. Try removing one or more optimization options and recompiling the function containing the line indicated in the error message.  
  
 You can probably fix the problem by removing one or more optimization options. To determine which option is at fault, remove options one at a time and recompile until the error message goes away. The options most commonly responsible are **/Og**, **/Oi**, and `/Oa`. Once you determine which option is responsible, you can disable it using the [optimize](../vs140/optimize.md) pragma around the function where the error occurs and continue to use the option for the rest of the module.  
  
 The Microsoft Knowledge Base has more information about C1001; see [http://support.microsoft.com/default.aspx?scid=kb;en-us;134650](http://support.microsoft.com/default.aspx?scid=kb;en-us;134650).  
  
 Try rewriting the line where the error is reported, or several lines of code surrounding that line.