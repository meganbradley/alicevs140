---
title: "Resource Compiler Error RC2001"
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
ms.assetid: 92bfb4c0-1879-4606-bb9f-ef7368707b4a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Compiler Error RC2001
newline in constant  
  
 A string constant was continued on a second line without either a backslash (**\\**) or closing and opening double quotation marks (**"**).  
  
 To break a string constant that is on two lines in the source file, do one of the following:  
  
-   End the first line with the line-continuation character, a backslash.  
  
-   Close the string on the first line with a double quotation mark and open the string on the next line with another quotation mark.  
  
 It is not sufficient to end the first line with \n, the escape sequence for embedding a newline character in a string constant.