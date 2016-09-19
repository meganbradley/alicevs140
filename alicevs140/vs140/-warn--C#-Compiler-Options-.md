---
title: "-warn (C# Compiler Options)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: /warn (C# Compiler Options)
ms.assetid: 5f80ff59-4991-4382-9f9a-77da18446e71
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -warn (C# Compiler Options)
The **/warn** option specifies the warning level for the compiler to display.  
  
## Syntax  
  
```  
/warn:option  
```  
  
## Arguments  
 `option`  
 The warning level you want displayed for the compilation: Lower numbers show only high severity warnings; higher numbers show more warnings. Valid values are 0-4:  
  
|Warning level|Meaning|  
|-------------------|-------------|  
|0|Turns off emission of all warning messages.|  
|1|Displays severe warning messages.|  
|2|Displays level 1 warnings plus certain, less-severe warnings, such as warnings about hiding class members.|  
|3|Displays level 2 warnings plus certain, less-severe warnings, such as warnings about expressions that always evaluate to `true` or `false`.|  
|4 (the default)|Displays all level 3 warnings plus informational warnings.|  
  
## Remarks  
 To get information about an error or warning, you can look up the error code in the Help Index. For other ways to get information about an error or warning, see [C# Compiler Errors](../vs140/C#-Compiler-Errors.md).  
  
 Use [/warnaserror](../Topic/-warnaserror%20\(C%23%20Compiler%20Options\).md) to treat all warnings as errors. Use [/nowarn](../vs140/-nowarn--C#-Compiler-Options-.md) to disable certain warnings.  
  
 **/w** is the short form of **/warn**.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Build** property page.  
  
3.  Modify the **Warning Level** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.WarningLevel?qualifyHint=False>.  
  
## Example  
 Compile `in.cs` and have the compiler only display level 1 warnings:  
  
```  
csc /warn:1 in.cs  
```  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)