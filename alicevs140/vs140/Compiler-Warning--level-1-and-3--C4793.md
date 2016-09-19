---
title: "Compiler Warning (level 1 and 3) C4793"
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
ms.topic: error-reference
ms.assetid: 819ada53-1d9c-49b8-a629-baf8c12314e6
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1 and 3) C4793
'function' : function is compiled as native code: 'reason'  
  
 The compiler cannot compile *function* into managed code, even though the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) compiler option is specified. Instead, the compiler emits warning C4793 and an explanatory continuation message, and then compiles *function* into native code. The continuation message contains the *reason* text that explains why *function* cannot be compiled to `MSIL`.  
  
 This is a level 1 warning when you specify the `/clr:pure` compiler option.  
  
 The following table lists all possible continuation messages.  
  
|Reason message|Remarks|  
|--------------------|-------------|  
|Aligned data types are not supported in managed code|The CLR must be able to allocate data as needed, which might not be possible if the data is aligned with declarations such as [__m128](../vs140/__m128.md) or [align](../vs140/align--C---.md).|  
|Functions that use '__ImageBase' are not supported in managed code|`__ImageBase` is a special linker symbol that is typically used only by low-level native code to load a DLL.|  
|varargs are not supported by the '/clr' compiler option|Native functions cannot call managed functions that have [variable argument lists](../vs140/Variable-Argument-Lists.md) (varargs) because the functions have different stack layout requirements. However, if you specify the `/clr:pure` compiler option, variable argument lists are supported because the assembly can contain only managed functions. For more information, see [Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md).|  
|The 64-bit CLR does not support data declared with the __ptr32 modifier|A pointer must be the same size as a native pointer on the current platform. For more information, see [__ptr32, \__ptr64](../vs140/__ptr32--__ptr64.md).|  
|The 32-bit CLR does not support data declared with the __ptr64 modifier|A pointer must be the same size as a native pointer on the current platform. For more information, see [__ptr32, \__ptr64](../vs140/__ptr32--__ptr64.md).|  
|One or more intrinsics is not supported in managed code|The name of the intrinsic is not available at the time the message is emitted. However, an intrinsic that causes this message typically represents a low-level machine instruction.|  
|Inline native assembly ('__asm') is not supported in managed code|[Inline assembly code](../vs140/__asm.md) can contain arbitrary native code, which cannot be managed.|  
|A non-__clrcall virtual function thunk must be compiled as native|A non-[__clrcall](../Topic/__clrcall.md) virtual function thunk must use an unmanaged address.|  
|A function using '_setjmp' must be compiled as native|The CLR must be able to control program execution. However, the [setjmp](../vs140/Using-setjmp-longjmp.md) function bypasses regular program execution by saving and restoring low-level information such as registers and execution state.|  
  
## Example  
 The following sample generates C4793.  
  
```  
// C4793.cpp  
// compile with: /c /clr /W3   
// processor: x86  
int asmfunc(void) {   // C4793, compiled as unmanaged, native code  
   __asm {  
      mov eax, 0  
   }  
}  
```  
  
 **warning C4793: 'asmfunc' : function is compiled as native code:**  
 **Inline native assembly ('__asm') is not supported in managed code**   
## Example  
 The following sample generates C4793.  
  
```  
// C4793_b.cpp  
// compile with: /c /clr /W3  
#include <setjmp.h>  
jmp_buf test_buf;  
  
void f() {  
   setjmp(test_buf);   // C4793 warning  
}  
```  
  
 **warning C4793: 'f' : function is compiled as native code:**  
 **A function using '_setjmp' must be compiled as native**