---
title: "OPTION (MASM)"
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
ms.assetid: 8e10dabd-e36f-4586-ab01-ada96736b0bd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OPTION (MASM)
Enables and disables features of the assembler.  
  
## Syntax  
  
```  
  
OPTION   
optionlist  
  
```  
  
## Remarks  
 Available options include:  
  
|||||  
|-|-|-|-|  
|**CASEMAP**|**DOTNAME**|**NODOTNAME**|**EMULATOR**|  
|**NOEMULATOR**|**EPILOGUE**|**EXPR16**|**EXPR32**|  
|**LANGUAGE**|**LJMP**|**NOLJMP**|**M510**|  
|**NOM510**|**NOKEYWORD**|**NOSIGNEXTEND**|**OFFSET**|  
|**OLDMACROS**|**NOOLDMACROS**|**OLDSTRUCTS**|**NOOLDSTRUCTS**|  
|**PROC**|**PROLOGUE**|**READONLY**|**NOREADONLY**|  
|**SCOPED**|**NOSCOPED**|**SEGMENT**|**SETIF2**.|  
  
 The syntax for LANGUAGE is **OPTION LANGUAGE:***x*, where *x* is one of C, SYSCALL, STDCALL, PASCAL, FORTRAN, or BASIC.  SYSCALL, PASCAL, FORTRAN, and BASIC are not supported with used with [.MODEL](../vs140/.MODEL.md) FLAT.  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)