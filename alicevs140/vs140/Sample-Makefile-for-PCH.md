---
title: "Sample Makefile for PCH"
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
ms.assetid: daf68983-77dc-45db-8701-aa89ad18910d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Sample Makefile for PCH
The following makefile uses macros and an !IF, !ELSE, !ENDIF flow-of-control command structure to simplify its adaptation to your project.  
  
```  
# Makefile : Illustrates the effective use of precompiled  
#            headers in a project  
# Usage:     NMAKE option  
# option:    DEBUG=[0|1]  
#            (DEBUG not defined is equivalent to DEBUG=0)  
#  
OBJS = myapp.obj applib.obj  
# List all stable header files in the STABLEHDRS macro.  
STABLEHDRS = stable.h another.h  
# List the final header file to be precompiled here:  
BOUNDRY = stable.h  
# List header files under development here:  
UNSTABLEHDRS = unstable.h  
# List all compiler options common to both debug and final  
# versions of your code here:  
CLFLAGS = /c /W3  
# List all linker options common to both debug and final  
# versions of your code here:  
LINKFLAGS = /NOD /ONERROR:NOEXE  
!IF "$(DEBUG)" == "1"  
CLFLAGS   = /D_DEBUG $(CLFLAGS) /Od /Zi /f  
LINKFLAGS = $(LINKFLAGS) /COD  
LIBS      = slibce  
!ELSE  
CLFLAGS   = $(CLFLAGS) /Oselg /Gs  
LINKFLAGS = $(LINKFLAGS)  
LIBS      = slibce  
!ENDIF  
myapp.exe: $(OBJS)  
    link $(LINKFLAGS) @<<  
$(OBJS), myapp, NUL, $(LIBS), NUL;  
<<  
# Compile myapp  
myapp.obj  : myapp.cpp $(UNSTABLEHDRS)  stable.pch  
    $(CPP) $(CLFLAGS) /Yu$(BOUNDRY)    myapp.cpp  
# Compile applib  
applib.obj : applib.cpp $(UNSTABLEHDRS) stable.pch  
    $(CPP) $(CLFLAGS) /Yu$(BOUNDRY)    applib.cpp  
# Compile headers  
stable.pch : $(STABLEHDRS)  
    $(CPP) $(CLFLAGS) /Yc$(BOUNDRY)    applib.cpp myapp.cpp  
```  
  
 Aside from the STABLEHDRS, BOUNDRY, and UNSTABLEHDRS macros shown in the figure "Structure of a Makefile That Uses a Precompiled Header File" in [PCH Files in the Build Process](../vs140/PCH-Files-in-the-Build-Process.md), this makefile provides a CLFLAGS macro and a LINKFLAGS macro. You must use these macros to list compiler and linker options that apply whether you build a debug or final version of the application's executable file. There is also a LIBS macro where you list the libraries your project requires.  
  
 The makefile also uses !IF, !ELSE, !ENDIF to detect whether you define a DEBUG symbol on the NMAKE command line:  
  
```  
NMAKE DEBUG=[1|0]  
```  
  
 This feature makes it possible for you to use the same makefile during development and for the final versions of your program — use DEBUG=0 for the final versions. The following command lines are equivalent:  
  
```  
NMAKE   
NMAKE DEBUG=0  
```  
  
 For more information on makefiles, see [NMAKE Reference](../vs140/NMAKE-Reference.md). Also see [Compiler Options](../vs140/Compiler-Options.md) and the [Linker Options](../Topic/Linker%20Options.md).  
  
## See Also  
 [Using Precompiled Headers in a Project](../vs140/Using-Precompiled-Headers-in-a-Project.md)