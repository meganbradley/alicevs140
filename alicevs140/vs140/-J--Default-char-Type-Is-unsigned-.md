---
title: "-J (Default char Type Is unsigned)"
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
H1: /J (Default char Type Is unsigned)
ms.assetid: 50973667-6638-491e-9c41-bff73acae19f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -J (Default char Type Is unsigned)
Changes the default `char` type from `signed char` to `unsigned char`, and the `char` type is zero-extended when it is widened to an `int` type.  
  
## Syntax  
  
```  
/J  
```  
  
## Remarks  
 If a `char` value is explicitly declared as `signed`, the **/J** option does not affect it, and the value is sign-extended when it is widened to an `int` type.  
  
 The **/J** option defines `_CHAR_UNSIGNED`, which is used with `#ifndef` in the LIMITS.h file to define the range of the default `char` type.  
  
 ANSI C and C++ do not require a specific implementation of the `char` type. This option is useful when you are working with character data that will eventually be translated into a language other than English.  
  
> [!NOTE]
>  If you use this compiler option with ATL/MFC, an error might be generated. Although you could disable this error by defining `_ATL_ALLOW_CHAR_UNSIGNED`, this workaround is not supported and may not always work.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  In **Solution Explorer**, open the shortcut menu for the project and then choose **Properties**.  
  
2.  In the project **Property Pages** dialog box, in the left pane under **Configuration Properties**, expand **C/C++** and then select **Command Line**.  
  
3.  In the **Additional Options** pane, specify the **/J** compiler option.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.DefaultCharIsUnsigned?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md)