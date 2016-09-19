---
title: "__asm"
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
ms.assetid: 77ff3bc9-a492-4b5e-85e1-fa4e414e79cd
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __asm
**Microsoft Specific**  
  
 The `__asm` keyword invokes the inline assembler and can appear wherever a C or C++ statement is legal. It cannot appear by itself. It must be followed by an assembly instruction, a group of instructions enclosed in braces, or, at the very least, an empty pair of braces. The term "`__asm` block" here refers to any instruction or group of instructions, whether or not in braces.  
  
> [!NOTE]
>  Visual C++ support for the Standard C++ `asm` keyword is limited to the fact that the compiler will not generate an error on the keyword. However, an `asm` block will not generate any meaningful code. Use `__asm` instead of `asm`.  
  
 Syntax:  
  
 __asm *assembly-instruction* [ ; ]  
  
 __asm { *assembly-instruction-list* } [ ; ]  
  
## Grammar  
 `__asm`  `assembly-instruction`  `;`opt  
  
 `__asm {`  `assembly-instruction-list`  `};`opt  
  
 *assembly-instruction-list*:  
 `assembly-instruction` `;`opt  
  
 `assembly-instruction` `;` `assembly-instruction-list` `;`opt  
  
 If used without braces, the `__asm` keyword means that the rest of the line is an assembly-language statement. If used with braces, it means that each line between the braces is an assembly-language statement. For compatibility with previous versions, `_asm` is a synonym for `__asm`.  
  
 Since the `__asm` keyword is a statement separator, you can put assembly instructions on the same line.  
  
 Before Visual C++ 2005, the instruction  
  
```  
__asm int 3  
```  
  
 did not cause native code to be generated when compiled with **/clr**; the compiler translated the instruction to a CLR break instruction.  
  
 `__asm int 3` now results in native code generation for the function. If you want a function to cause a break point in your code and if you want that function compiled to MSIL, use [__debugbreak](../vs140/__debugbreak.md).  
  
## Example  
 The following code fragment is a simple `__asm` block enclosed in braces:  
  
```  
__asm {  
   mov al, 2  
   mov dx, 0xD007  
   out dx, al  
}  
```  
  
 Alternatively, you can put `__asm` in front of each assembly instruction:  
  
```  
__asm mov al, 2  
__asm mov dx, 0xD007  
__asm out dx, al  
```  
  
 Because the `__asm` keyword is a statement separator, you can also put assembly instructions on the same line:  
  
```  
__asm mov al, 2   __asm mov dx, 0xD007   __asm out dx, al  
```  
  
 All three examples generate the same code, but the first style (enclosing the `__asm` block in braces) has some advantages. The braces clearly separate assembly code from C or C++ code and avoid needless repetition of the `__asm` keyword. Braces can also prevent ambiguities. If you want to put a C or C++ statement on the same line as an `__asm` block, you must enclose the block in braces. Without the braces, the compiler cannot tell where assembly code stops and C or C++ statements begin. Finally, because the text in braces has the same format as ordinary MASM text, you can easily cut and paste text from existing MASM source files.  
  
 Unlike braces in C and C++, the braces enclosing an `__asm` block don't affect variable scope. You can also nest `__asm` blocks; nesting does not affect variable scope.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [Inline Assembler](../vs140/Inline-Assembler.md)