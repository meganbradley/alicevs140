---
title: "Support for Using wmain"
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
ms.assetid: 41213c41-668c-40a4-8a1e-77d9eded720d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Support for Using wmain
Visual C++ supports defining a **wmain** function and passing wide-character arguments to your Unicode application. You declare formal parameters to **wmain**, using a format similar to **main**. You can then pass wide-character arguments and, optionally, a wide-character environment pointer to the program. The `argv` and `envp` parameters to **wmain** are of type `wchar_t*`. For example:  
  
```  
wmain( int argc, wchar_t *argv[ ], wchar_t *envp[ ] )  
```  
  
> [!NOTE]
>  MFC Unicode applications use **wWinMain** as the entry point. In this case, `CWinApp::m_lpCmdLine` is a Unicode string. Be sure to set **wWinMainCRTStartup** with the [/ENTRY](../vs140/-ENTRY--Entry-Point-Symbol-.md) linker option.  
  
 If your program uses a **main** function, the multibyte-character environment is created by the run-time library at program startup. A wide-character copy of the environment is created only when needed (for example, by a call to the `_wgetenv` or `_wputenv` functions). On the first call to `_wputenv`, or on the first call to `_wgetenv` if an MBCS environment already exists, a corresponding wide-character string environment is created. The environment is then pointed to by the `_wenviron` global variable, which is a wide-character version of the `_environ` global variable. At this point, two copies of the environment (MBCS and Unicode) exist simultaneously and are maintained by the run-time system throughout the life of the program.  
  
 Similarly, if your program uses a **wmain** function, a wide-character environment is created at program startup and is pointed to by the `_wenviron` global variable. An MBCS (ASCII) environment is created on the first call to `_putenv` or `getenv` and is pointed to by the `_environ` global variable.  
  
## See Also  
 [Support for Unicode](../vs140/Support-for-Unicode.md)   
 [Unicode Programming Summary](../vs140/Unicode-Programming-Summary.md)   
 [WinMain Function](http://msdn.microsoft.com/library/windows/desktop/ms633559)