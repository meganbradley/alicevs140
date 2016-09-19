---
title: "CONSTRUCTOR_ENUM"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d335b2c-66bc-460c-a4a6-4f3f1b697c2c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# CONSTRUCTOR_ENUM
Selects different types of constructors.  
  
## Syntax  
  
```cpp#  
typedef enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
} CONSTRUCTOR_ENUM;  
```  
  
```c#  
public enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
};  
```  
  
## Members  
 crAll  
 Selects all constructors.  
  
 crNonStatic  
 Selects non-static constructors.  
  
 crStatic  
 Selects static constructors.  
  
## Remarks  
 Passed as an argument to the [EnumConstructors](../vs140/IDebugClassField--EnumConstructors.md) method.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetReason](../vs140/IDebugCanStopEvent2--GetReason.md)