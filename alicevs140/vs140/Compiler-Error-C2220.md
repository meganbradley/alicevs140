---
title: "Compiler Error C2220"
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
ms.assetid: d610802c-64d7-40ad-a2a6-0ed0b6815a6c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2220
warning treated as error - no object file generated  
  
 [/WX](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) tells the compiler to treat all warnings as errors. Because an error occurred, no object or executable file was generated.  
  
 This error only appears when the **/WX** flag is set and a warning occurs during compilation. To fix this error, you must eliminate every warning in your project.  
  
### To fix, use one of the following techniques  
  
-   Fix the problems that cause warnings in your project.  
  
-   Compile at a lower warning level—for example, use **/W3** instead of **/W4**.  
  
-   Use a [warning](../vs140/warning.md) pragma to disable or suppress a specific warning.  
  
-   Don't use **/WX** to compile.