---
title: "_ATL_ENABLE_PTM_WARNING"
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
ms.topic: reference
ms.assetid: 00b9ff5c-9834-4c40-911e-ee88d512c4af
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_ENABLE_PTM_WARNING
Define this macro in order to force the use of ANSI C++ standard-compliant syntax for pointer to member functions. Using this macro will cause the C4867 compiler error to be generated when non-standard syntax is used to initialize a pointer to a member function.  
  
## Syntax  
  
```  
  
#define _ATL_ENABLE_PTM_WARNING  
  
```  
  
## Remarks  
 The ATL and MFC libraries have been changed to match the Visual C++ compiler's improved standard C++ compliance. According to the ANSI C++ standard, the syntax of a pointer to a class member function should be `&CMyClass::MyFunc`.  
  
 When [_ATL_ENABLE_PTM_WARNING](../vs140/_ATL_ENABLE_PTM_WARNING.md) is not defined (the default case), ATL/MFC disables the C4867 error in macro maps (notably message maps) so that code that was created in earlier versions can continue to build as before. If you define **_ATL_ENABLE_PTM_WARNING**, your code should be C++ standard compliant.  
  
 However, the non-standard form has been deprecated, so you need to move existing code to C++ standard compliant syntax. For example, the following:  
  
 [!CODE [NVC_MFCListView#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#14)]  
  
 Should be changed to:  
  
 [!CODE [NVC_MFCListView#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#11)]  
  
 Note that for map macros that add the '&' character, you should not add it again in your code.  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [Compiler Warning C4867](../vs140/Compiler-Warning-C4867.md)