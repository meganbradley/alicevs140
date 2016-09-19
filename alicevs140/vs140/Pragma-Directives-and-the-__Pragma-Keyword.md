---
title: "Pragma Directives and the __Pragma Keyword"
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
ms.assetid: 9867b438-ac64-4e10-973f-c3955209873f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Pragma Directives and the __Pragma Keyword
Pragma directives specify machine- or operating-specific compiler features. The `__pragma` keyword, which is specific to the Microsoft compiler, enables you to code pragma directives within macro definitions.  
  
## Syntax  
  
```  
  
      #pragma token-string  
__pragma(token-string)  
```  
  
## Remarks  
 Each implementation of C and C++ supports some features unique to its host machine or operating system. Some programs, for example, must exercise precise control over the memory areas where data is put or to control the way certain functions receive parameters. The `#pragma` directives offer a way for each compiler to offer machine- and operating system-specific features while retaining overall compatibility with the C and C++ languages.  
  
 Pragmas are machine- or operating system-specific by definition, and are usually different for every compiler. Pragmas can be used in conditional statements, to provide new preprocessor functionality, or to provide implementation-defined information to the compiler.  
  
 The `token-string` is a series of characters that gives a specific compiler instruction and arguments, if any. The number sign (**#**) must be the first non-white-space character on the line that contains the pragma; white-space characters can separate the number sign and the word "pragma". Following `#pragma`, write any text that the translator can parse as preprocessing tokens. The argument to `#pragma` is subject to macro expansion.  
  
 If the compiler finds a pragma that it does not recognize, it issues a warning and continues compilation.  
  
 The Microsoft C and C++ compilers recognize the following pragmas:  
  
||||  
|-|-|-|  
|[alloc_text](../vs140/alloc_text.md)|[auto_inline](../vs140/auto_inline.md)|[bss_seg](../vs140/bss_seg.md)|  
|[check_stack](../vs140/check_stack.md)|[code_seg](../vs140/code_seg.md)|[comment](../vs140/comment--C-C---.md)|  
|[component](../vs140/component.md)|[conform](../vs140/conform.md) <sup>1</sup>|[const_seg](../vs140/const_seg.md)|  
|[data_seg](../vs140/data_seg.md)|[deprecated](../vs140/deprecated--C-C---.md)|[detect_mismatch](../vs140/detect_mismatch.md)|  
|[fenv_access](../vs140/fenv_access.md)|[float_control](../vs140/float_control.md)|[fp_contract](../vs140/fp_contract.md)|  
|[function](../vs140/function--C-C---.md)|[hdrstop](../vs140/hdrstop.md)|[include_alias](../vs140/include_alias.md)|  
|[init_seg](../vs140/init_seg.md) <sup>1</sup>|[inline_depth](../vs140/inline_depth.md)|[inline_recursion](../vs140/inline_recursion.md)|  
|[intrinsic](../vs140/intrinsic.md)|[loop](../vs140/loop.md) <sup>1</sup>|[make_public](../vs140/make_public.md)|  
|[managed](../vs140/managed--unmanaged.md)|[message](../vs140/message.md)||  
|[omp](../vs140/omp.md)|[once](../vs140/once.md)||  
|[optimize](../vs140/optimize.md)|[pack](../vs140/pack.md)|[pointers_to_members](../vs140/pointers_to_members.md) <sup>1</sup>|  
|[pop_macro](../vs140/pop_macro.md)|[push_macro](../vs140/push_macro.md)|[region, endregion](../vs140/region--endregion.md)|  
|[runtime_checks](../vs140/runtime_checks.md)|[section](../vs140/section.md)|[setlocale](../vs140/setlocale.md)|  
|[strict_gs_check](../vs140/strict_gs_check.md)|[unmanaged](../vs140/managed--unmanaged.md)|[vtordisp](../vs140/vtordisp.md) <sup>1</sup>|  
|[warning](../vs140/warning.md)|||  
  
 1. Supported only by the C++ compiler.  
  
## Pragmas and Compiler Options  
 Some pragmas provide the same functionality as compiler options. When a pragma is encountered in source code, it overrides the behavior specified by the compiler option. For example, if you specified [/Zp8](../Topic/-Zp%20\(Struct%20Member%20Alignment\).md), you can override this compiler setting for specific sections of the code with [pack](../vs140/pack.md):  
  
```  
cl /Zp8 ...  
  
<file> - packing is 8  
// ...  
#pragma pack(push, 1) - packing is now 1  
// ...  
#pragma pack(pop) - packing is 8  
</file>  
```  
  
## The __pragma() Keyword  
 **Microsoft specific**  
  
 The compiler also supports the `__pragma` keyword, which has the same functionality as the `#pragma` directive, but can be used inline in a macro definition. The `#pragma` directive cannot be used in a macro definition because the compiler interprets the number sign character ('#') in the directive to be the [stringizing operator (#)](../vs140/Stringizing-Operator--#-.md).  
  
 The following code example demonstrates how the `__pragma` keyword can be used in a macro. This code is excerpted from the mfcdual.h header in the ACDUAL sample in "Compiler COM Support Samples":  
  
```  
#define CATCH_ALL_DUAL \  
CATCH(COleException, e) \  
{ \  
_hr = e->m_sc; \  
} \  
AND_CATCH_ALL(e) \  
{ \  
__pragma(warning(push)) \  
__pragma(warning(disable:6246)) /*disable _ctlState prefast warning*/ \  
AFX_MANAGE_STATE(pThis->m_pModuleState); \  
__pragma(warning(pop)) \  
_hr = DualHandleException(_riidSource, e); \  
} \  
END_CATCH_ALL \  
return _hr; \  
```  
  
 **End Microsoft specific**  
  
## See Also  
 [C/C++ Preprocessor Reference](../vs140/C-C---Preprocessor-Reference.md)   
 [C Pragmas](../vs140/C-Pragmas.md)   
 [C++ Keywords](../vs140/Keywords--C---.md)