---
title: "Calling Example: Function Prototype and Call"
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
ms.topic: language-reference
ms.assetid: e4275d1f-df2e-4bfc-a162-eb43ec69554a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Calling Example: Function Prototype and Call
## Microsoft Specific  
 The following example shows the results of making a function call using various calling conventions.  
  
 This example is based on the following function skeleton. Replace `calltype` with the appropriate calling convention.  
  
```  
void    calltype MyFunc( char c, short s, int i, double f );  
.  
.  
.  
void    MyFunc( char c, short s, int i, double f )  
    {  
    .  
    .  
    .  
    }  
.  
.  
.  
MyFunc ('x', 12, 8192, 2.7183);  
```  
  
 For more information, see [Results of Calling Example](../vs140/Results-of-Calling-Example.md).  
  
## END Microsoft Specific  
  
## See Also  
 [Calling Conventions](../vs140/Calling-Conventions.md)