---
title: "Resource Compiler Warning RC4005"
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
ms.assetid: 71f03b4a-c9a9-415d-920f-bf2e58507f93
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Compiler Warning RC4005
'identifier' : macro redefinition  
  
 The identifier is defined twice. The compiler used the second macro definition.  
  
 This warning can be caused by defining a macro on the command line and in the code with a `#define` directive. It also can be caused by macros imported from include files.  
  
 To eliminate the warning, either remove one of the definitions or use an `#undef` directive before the second definition.