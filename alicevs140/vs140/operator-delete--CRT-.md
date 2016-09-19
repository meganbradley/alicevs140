---
title: "operator delete (CRT)"
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
apilocation: 
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: bcd0066a-0022-45f5-af4c-9007c64a6b89
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator delete (CRT)
Frees allocated block.  
  
## Syntax  
  
```  
  
      void __cdecl operator delete(  
   void * object  
);  
void __cdecl operator delete(  
   void * object,   
   void * memory  
) throw();  
void __cdecl operator delete(  
   void * object,   
   const std::nothrow_t&  
) throw();  
```  
  
#### Parameters  
 *memory*  
 The memory location being freed.  
  
 *object*  
 A pointer to the object being deleted.  
  
## Remarks  
 This form of **operator delete** is known as scalar delete, in contrast to the vector delete form ([operator delete&#91;&#93;](../vs140/operator-delete-CRT-.md)).  
  
 **operator delete** frees memory allocated by [operator new](../vs140/operator-new--CRT-.md).  
  
 The first form of this operator is known as the nonplacement form. The second and third forms of this operator will commonly not be called from code but exist to give the compiler a matching delete to call when a placement new fails.  
  
 The first form of the operator is defined by the compiler and does not require new.h to be included in your program.  
  
 With the exception of throwing or no-throwing behavior, the CRT **operator delete** behaves like [operator delete](../vs140/operator-delete---new--.md) in the Standard C++ Library.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|**delete**|<new.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
 See [operator new](../vs140/operator-new--CRT-.md) for examples of using operator **delete**.  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)