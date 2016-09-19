---
title: "hdrstop"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5ea8370a-10d1-4538-ade6-4c841185da0e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hdrstop
Gives you additional control over precompilation file names and over the location at which the compilation state is saved.  
  
## Syntax  
  
```  
  
#pragma hdrstop [( "filename" )]    
```  
  
## Remarks  
 The *filename* is the name of the precompiled header file to use or create (depending on whether [/Yu](../vs140/-Yu--Use-Precompiled-Header-File-.md) or [/Yc](../vs140/-Yc--Create-Precompiled-Header-File-.md) is specified). If *filename* does not contain a path specification, the precompiled header file is assumed to be in the same directory as the source file.  
  
 If a C or C++ file contains a **hdrstop** pragma when compiled with /Yc, the compiler saves the state of the compilation up to the location of the pragma. The compiled state of any code that follows the pragma is not saved.  
  
 Use *filename* to name the precompiled header file in which the compiled state is saved. A space between **hdrstop** and *filename* is optional. The file name specified in the **hdrstop** pragma is a string and is therefore subject to the constraints of any C or C++ string. In particular, you must enclose it in quotation marks and use the escape character (backslash) to specify directory names. For example:  
  
```  
#pragma hdrstop( "c:\\projects\\include\\myinc.pch" )  
```  
  
 The name of the precompiled header file is determined according to the following rules, in order of precedence:  
  
1.  The argument to the /Fp compiler option  
  
2.  The *filename* argument to #**pragma hdrstop**  
  
3.  The base name of the source file with a .PCH extension  
  
 For the /Yc and /Yu options, if neither of the two compilation options nor the **hdrstop** pragma specifies a file name, the base name of the source file is used as the base name of the precompiled header file.  
  
 You can also use preprocessing commands to perform macro replacement as follows:  
  
```  
#define INCLUDE_PATH "c:\\progra~`1\\devstsu~1\\vc\\include\\"  
#define PCH_FNAME "PROG.PCH"  
.  
.  
.  
#pragma hdrstop( INCLUDE_PATH PCH_FNAME )  
```  
  
 The following rules govern where the **hdrstop** pragma can be placed:  
  
-   It must appear outside any data or function declaration or definition.  
  
-   It must be specified in the source file, not within a header file.  
  
## Example  
  
```  
#include <windows.h>                 // Include several files  
#include "myhdr.h"  
  
__inline Disp( char *szToDisplay )   // Define an inline function  
{  
    ...                              // Some code to display string  
}  
#pragma hdrstop  
```  
  
 In this example, the **hdrstop** pragma appears after two files have been included and an inline function has been defined. This might, at first, seem to be an odd placement for the pragma. Consider, however, that using the manual precompilation options, /Yc and /Yu, with the **hdrstop** pragma makes it possible for you to precompile entire source files — even inline code. The Microsoft compiler does not limit you to precompiling only data declarations.  
  
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)