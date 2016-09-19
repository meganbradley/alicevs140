---
title: "-sdl (Enable Additional Security Checks)"
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
H1: /sdl (Enable Additional Security Checks)
ms.assetid: 3dcf86a0-3169-4240-9f29-e04a9f535826
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -sdl (Enable Additional Security Checks)
Adds recommended Security Development Lifecycle (SDL) checks. These checks include extra security-relevant warnings as errors, and additional secure code-generation features.  
  
## Syntax  
  
```  
/sdl[-]  
```  
  
## Remarks  
 **/sdl** enables a superset of the baseline security checks provided by [/GS](../Topic/-GS%20\(Buffer%20Security%20Check\).md) and overrides **/GS-**. By default, **/sdl** is off. **/sdl-** disables the additional security checks.  
  
## Compile-time Checks  
 **/sdl** enables these warnings as errors:  
  
|Warning enabled by /sdl|Equivalent command-line switch|Description|  
|------------------------------|-------------------------------------|-----------------|  
|[C4146](../vs140/Compiler-Warning--level-2--C4146.md)|/we4146|A unary minus operator was applied to an unsigned type, resulting in an unsigned result.|  
|[C4308](../vs140/Compiler-Warning--level-2--C4308.md)|/we4308|A negative integral constant converted to unsigned type, resulting in a possibly meaningless result.|  
|[C4532](../vs140/Compiler-Warning--level-1--C4532.md)|/we4532|Use of `continue`, `break` or `goto` keywords in a `__finally`/`finally` block has undefined behavior during abnormal termination.|  
|[C4533](../vs140/Compiler-Warning--level-1--C4533.md)|/we4533|Code initializing a variable will not be executed.|  
|[C4700](../vs140/Compiler-Warning--level-1-and-level-4--C4700.md)|/we4700|Use of an uninitialized local variable.|  
|[C4703](../vs140/Compiler-Warning--level-4--C4703.md)|/we4703|Use of a potentially uninitialized local pointer variable.|  
|[C4789](../vs140/Compiler-Warning--Level-1--C4789.md)|/we4789|Buffer overrun when specific C run-time (CRT) functions are used.|  
|[C4995](../vs140/Compiler-Warning--level-3--C4995.md)|/we4995|Use of a function marked with pragma [deprecated](../vs140/deprecated--C-C---.md).|  
|[C4996](../vs140/Compiler-Warning--level-3--C4996.md)|/we4996|Use of a function marked as [deprecated](../vs140/deprecated--C---.md).|  
  
## Runtime checks  
 When **/sdl** is enabled, the compiler generates code to perform these checks at run time:  
  
-   Enables the strict mode of **/GS** run-time buffer overrun detection, equivalent to compiling with `#pragma strict_gs_check(push, on)`.  
  
-   Performs limited pointer sanitization. In expressions that do not involve dereferences and in types that have no user-defined destructor, pointer references are set to a non-valid address after a call to `delete`. This helps to prevent the reuse of stale pointer references.  
  
-   Performs class member initialization. Automatically initializes all class members to zero on object instantiation (before the constructor runs). This helps prevent the use of uninitialized data associated with class members that the constructor does not explicitly initialize.  
  
## Remarks  
 For more information, see [Warnings, /sdl, and improving uninitialized variable detection](http://go.microsoft.com/fwlink/p/?LinkId=331012).  
  
#### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Select the **C/C++** folder.  
  
3.  On the **General** page, select the option from the **SDL checks** drop-down list.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)