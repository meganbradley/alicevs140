---
title: "Windows Runtime Unsupported CRT Functions"
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
ms.assetid: bb8386d6-0ef8-460c-88d8-addff009b6f1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Runtime Unsupported CRT Functions
Many C run-time (CRT) APIs can’t be used in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. These apps are built by using the /ZW compiler flag. For a list of unsupported CRT functions, see [CRT functions not supported by /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
 All CRT APIs are described in the [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md) section of the documentation.  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)   
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)