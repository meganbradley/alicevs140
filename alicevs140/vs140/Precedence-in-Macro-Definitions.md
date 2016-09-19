---
title: "Precedence in Macro Definitions"
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
ms.assetid: 0c13182d-83cb-4cbd-af2d-f4c916b62aeb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Precedence in Macro Definitions
If a macro has multiple definitions, NMAKE uses the highest-precedence definition. The following list shows the order of precedence, from highest to lowest:  
  
1.  A macro defined on the command line  
  
2.  A macro defined in a makefile or include file  
  
3.  An inherited environment-variable macro  
  
4.  A macro defined in the Tools.ini file  
  
5.  A predefined macro, such as [CC](../vs140/Command-Macros-and-Options-Macros.md) and [AS](../vs140/Command-Macros-and-Options-Macros.md)  
  
 Use /E to cause macros inherited from environment variables to override makefile macros with the same name. Use **!UNDEF** to override a command line.  
  
## See Also  
 [Defining an NMAKE Macro](../vs140/Defining-an-NMAKE-Macro.md)