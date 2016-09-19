---
title: "How to: Marshal COM Strings Using C++ Interop"
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
ms.topic: get-started-article
ms.assetid: 06590759-bf99-4e34-a3a9-4527ea592cc2
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Marshal COM Strings Using C++ Interop
This topic demonstrates how a BSTR (the basic string format favored in COM programming) can be passed from a managed to an unmanaged function, and vice versa. For interoperating with other strings types, see the following topics:  
  
-   [How to: Marshal Unicode Strings Using C++ Interop](../Topic/How%20to:%20Marshal%20Unicode%20Strings%20Using%20C++%20Interop.md)  
  
-   [How to: Marshal ANSI Strings Using C++ Interop](../Topic/How%20to:%20Marshal%20ANSI%20Strings%20Using%20C++%20Interop.md)  
  
 The following code examples use the [managed, unmanaged](../vs140/managed--unmanaged.md) #pragma directives to implement managed and unmanaged functions in the same file, but these functions interoperate in the same manner if defined in separate files. Files containing only unmanaged functions do not need to be compiled with [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
## Example  
 The following example demonstrates how a BSTR (a string format used in COM programming) can be passed from a managed to an unmanaged function. The calling managed function uses <xref:System.Runtime.InteropServices.Marshal.StringToBSTR?qualifyHint=False> to obtain the address of a BSTR representation of the contents of a .NET System.String. This pointer is pinned using [pin_ptr](../vs140/pin_ptr--C---CLI-.md) to ensure that its physical address is not changed during a garbage collection cycle while the unmanaged function executes. The garbage collector is prohibited from moving the memory until the [pin_ptr](../vs140/pin_ptr--C---CLI-.md) goes out of scope.  
  
```  
// MarshalBSTR1.cpp  
// compile with: /clr  
#define WINVER 0x0502  
#define _AFXDLL  
#include <afxwin.h>  
  
#include <iostream>  
using namespace std;  
  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
#pragma unmanaged  
  
void NativeTakesAString(BSTR bstr) {  
   printf_s("%S", bstr);  
}  
  
#pragma managed  
  
int main() {  
   String^ s = "test string";  
  
   IntPtr ip = Marshal::StringToBSTR(s);  
   BSTR bs = static_cast<BSTR>(ip.ToPointer());  
   pin_ptr<BSTR> b = &bs;  
  
   NativeTakesAString( bs );  
   Marshal::FreeBSTR(ip);  
}  
```  
  
## Example  
 The following example demonstrates how a BSTR can be passed from an unmanaged to an unmanaged function. The receiving managed function can either use the string in as a BSTR or use <xref:System.Runtime.InteropServices.Marshal.PtrToStringBSTR?qualifyHint=False> to convert it to a <xref:System.String?qualifyHint=False> for use with other managed functions. Because the memory representing the BSTR is allocated on the unmanaged heap, no pinning is necessary, because there is no garbage collection on the unmanaged heap.  
  
```  
// MarshalBSTR2.cpp  
// compile with: /clr  
#define WINVER 0x0502  
#define _AFXDLL  
#include <afxwin.h>  
  
#include <iostream>  
using namespace std;  
  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
#pragma managed  
  
void ManagedTakesAString(BSTR bstr) {  
   String^ s = Marshal::PtrToStringBSTR(static_cast<IntPtr>(bstr));  
   Console::WriteLine("(managed) convered BSTR to String: '{0}'", s);  
}  
  
#pragma unmanaged  
  
void UnManagedFunc() {  
   BSTR bs = SysAllocString(L"test string");  
   printf_s("(unmanaged) passing BSTR to managed func...\n");  
   ManagedTakesAString(bs);  
}  
  
#pragma managed  
  
int main() {  
   UnManagedFunc();  
}  
```  
  
## See Also  
 [Using C++ Interop Features](../vs140/Using-C---Interop--Implicit-PInvoke-.md)