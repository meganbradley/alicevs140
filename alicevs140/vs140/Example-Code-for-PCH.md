---
title: "Example Code for PCH"
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
ms.assetid: 4e3b97b2-e087-49a7-ab50-c6e8723a436e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Example Code for PCH
The following examples are used in the makefile described in [PCH Files in the Build Process](../vs140/PCH-Files-in-the-Build-Process.md) and [Sample Makefile for PCH](../vs140/Sample-Makefile-for-PCH.md). Note that the comments contain important information.  
  
```  
// ANOTHER.H : Contains the interface to code that is not  
//             likely to change.  
//  
#ifndef --ANOTHER_H  
#define --ANOTHER_H  
#include<iostream>  
void savemoretime( void );  
#endif // --ANOTHER_H  
  
// STABLE.H : Contains the interface to code that is not likely  
//            to change. List code that is likely to change   
//            in the makefile's STABLEHDRS macro.  
//  
#ifndef --STABLE_H  
#define --STABLE_H  
#include<iostream>  
void savetime( void );  
#endif // --STABLE_H  
  
// UNSTABLE.H : Contains the interface to code that is  
//              likely to change. As the code in a header  
//              file becomes stable, remove the header file  
//              from the makefile's UNSTABLEHDR macro and list  
//              it in the STABLEHDRS macro.  
//  
#ifndef --UNSTABLE_H  
#define --UNSTABLE_H  
#include<iostream.h>  
void notstable( void );  
#endif // --UNSTABLE_H  
  
// APPLIB.CPP : This file contains the code that implements  
//              the interface code declared in the header  
//              files STABLE.H, ANOTHER.H, and UNSTABLE.H.  
//  
#include"another.h"  
#include"stable.h"  
#include"unstable.h"  
// The following code represents code that is deemed stable and  
// not likely to change. The associated interface code is  
// precompiled. In this example, the header files STABLE.H and  
// ANOTHER.H are precompiled.  
void savetime( void )  
    { cout << "Why recompile stable code?\n"; }  
void savemoretime( void )  
    { cout << "Why, indeed?\n\n"; }  
// The following code represents code that is still under  
// development. The associated header file is not precompiled.  
void notstable( void )  
    { cout << "Unstable code requires"  
            << " frequent recompilation.\n"; }  
  
// MYAPP.CPP : Sample application  
//             All precompiled code other than the file listed  
//             in the makefile's BOUNDRY macro (stable.h in  
//             this example) must be included before the file  
//             listed in the BOUNDRY macro. Unstable code must  
//             be included after the precompiled code.  
//  
#include"another.h"  
#include"stable.h"  
#include"unstable.h"  
int main( void )  
{  
    savetime();  
    savemoretime();  
    notstable();  
}  
```  
  
## See Also  
 [Using Precompiled Headers in a Project](../vs140/Using-Precompiled-Headers-in-a-Project.md)