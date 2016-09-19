---
title: "Compiler Warning (level 3) C4792"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c047ce69-a622-44e1-9425-d41aa9261c61
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4792
function 'function' declared using sysimport and referenced from native code; import library required to link  
  
 A native function that was imported into the program with DllImport was called from an unmanaged function. Therefore, you must link to the import library for the DLL.  
  
 This warning cannot be resolved in code or by changing the way you compile. Use the [warning](../vs140/warning.md) pragma to disable this warning.  
  
 The following sample generates C4792:  
  
```  
// C4792.cpp  
// compile with: /clr /W3  
// C4792 expected  
using namespace System::Runtime::InteropServices;  
[DllImport("msvcrt")]  
extern "C" int __cdecl puts(const char *);  
int main() {}  
  
// Uncomment the following line to resolve.  
// #pragma warning(disable : 4792)  
#pragma unmanaged  
void func(void){  
   puts("test");  
}  
```