---
title: "ASSUME"
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
ms.assetid: cd162070-aee9-4c65-babc-005c6cc73d7c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ASSUME
Enables error checking for register values.  
  
## Syntax  
  
```  
  
      ASSUME segregister:name [[, segregister:name]]...  
ASSUME dataregister:type [[, dataregister:type]]...  
ASSUME register:ERROR [[, register:ERROR]]...  
ASSUME [[register:]] NOTHING [[, register:NOTHING]]...  
```  
  
## Remarks  
 After an `ASSUME` is put into effect, the assembler watches for changes to the values of the given registers. **ERROR** generates an error if the register is used. **NOTHING** removes register error checking. You can combine different kinds of assumptions in one statement.  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)