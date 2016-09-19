---
title: "Using C++ Interop (Implicit PInvoke)"
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
ms.assetid: 5f710bf1-88ae-4c4e-8326-b3f0b7c4c68a
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using C++ Interop (Implicit PInvoke)
Unlike other .NET languages, Visual C++ has interoperability support that allows managed and unmanaged code to exist in the same application and even in the same file (with the [managed, unmanaged](../vs140/managed--unmanaged.md) pragmas). This allows Visual C++ developers to integrate .NET functionality into existing Visual C++ applications without disturbing the rest of the application.  
  
 You can also call unmanaged functions from a managed compiland using [dllexport, dllimport](../vs140/dllexport--dllimport.md).  
  
 Implicit PInvoke is useful when you do not need to specify how function parameters will be marshaled, or any of the other details that can be specified when explicitly calling DllImportAttribute.  
  
 Visual C++ provides two ways for managed and unmanaged functions to interoperate:  
  
-   [Using Explicit PInvoke in C++ (Using the DllImport Attribute)](../Topic/Using%20Explicit%20PInvoke%20in%20C++%20\(DllImport%20Attribute\).md)  
  
 Explicit PInvoke is supported by the .NET Framework and is available in most .NET languages. But as its name implies, C++ Interop is specific to Visual C++.  
  
## C++ Interop  
 C++ Interop is recommended over explicit PInvoke because it provides better type safety, is typically less tedious to implement, is more forgiving if the unmanaged API is modified, and makes performance enhancements possible that are not possible with explicit PInvoke. However, C++ Interop is not possible if the unmanaged source code is not available or when compiling with **/clr:safe** (see [Pure / Verifiable](../vs140/Pure-and-Verifiable-Code--C---CLI-.md) for more information).  
  
## C++ COM Interop  
 The interoperability features supported by Visual C++ offer a particular advantage over other .NET languages when it comes to interoperating with COM components. Instead of being limited to the restrictions of the .NET Framework [Type Library Importer (Tlbimp.exe)](assetId:///ec0a8d63-11b3-4acd-b398-da1e37e97382), such as limited support for data types and the mandatory exposure of every member of every COM interface, C++ Interop allows COM components to be accessed at will and does not require separate interop assemblies. For more information, see [Using COM from .NET](assetId:///03976661-6278-4227-a6c1-3b3315502c15).  
  
## Blittable Types  
 For unmanaged APIs that use simple, intrinsic types (see [Blittable and Non-Blittable Types](assetId:///d03b050e-2916-49a0-99ba-f19316e5c1b3)), no special coding is required because these data types have the same representation in memory, but more complex data types require explicit data marshaling. For an example, see [How to: Call Native DLLs from Managed Code (P/Invoke)](../vs140/How-to--Call-Native-DLLs-from-Managed-Code-Using-PInvoke.md).  
  
## Example  
  
```  
// vcmcppv2_impl_dllimp.cpp  
// compile with: /clr:pure user32.lib  
using namespace System::Runtime::InteropServices;  
  
// Implicit DLLImport specifying calling convention  
extern "C" int __stdcall MessageBeep(int);  
  
// explicit DLLImport needed here to use P/Invoke marshalling because  
// System::String ^ is not the type of the first parameter to printf  
[DllImport("msvcrt.dll", EntryPoint = "printf", CallingConvention = CallingConvention::Cdecl,  CharSet = CharSet::Ansi)]  
// or just  
// [DllImport("msvcrt.dll")]  
int printf(System::String ^, ...);   
  
int main() {  
   // (string literals are System::String by default)  
   printf("Begin beep\n");  
   MessageBeep(100000);  
   printf("Done\n");  
}  
```  
  
 **Begin beep**  
**Done**   
## In This Section  
  
-   [How to: Marshal ANSI Strings using C++ Interop](../Topic/How%20to:%20Marshal%20ANSI%20Strings%20Using%20C++%20Interop.md)  
  
-   [How to: Marshal Unicode Strings using C++ Interop](../Topic/How%20to:%20Marshal%20Unicode%20Strings%20Using%20C++%20Interop.md)  
  
-   [How to: Marshal COM Strings using C++ Interop](../vs140/How-to--Marshal-COM-Strings-Using-C---Interop.md)  
  
-   [How to: Marshal Structures using C++ Interop](../vs140/How-to--Marshal-Structures-Using-C---Interop.md)  
  
-   [How to: Marshal Arrays using C++ Interop](../vs140/How-to--Marshal-Arrays-Using-C---Interop.md)  
  
-   [How to: Marshal Callbacks and Delegates using C++ Interop](../Topic/How%20to:%20Marshal%20Callbacks%20and%20Delegates%20By%20Using%20C++%20Interop.md)  
  
-   [How to: Marshal Embedded Pointers using C++ Interop](../vs140/How-to--Marshal-Embedded-Pointers-Using-C---Interop.md)  
  
-   [How to: Access Characters in a System::String](../vs140/How-to--Access-Characters-in-a-System--String.md)  
  
-   [How to: Convert char * String to System::Byte Array](../Topic/How%20to:%20Convert%20char%20*%20String%20to%20System::Byte%20Array.md)  
  
-   [How to: Convert System::String to wchar_t* or char\*](../vs140/How-to--Convert-System--String-to-wchar_t--or-char-.md)  
  
-   [How to: Convert System::String to Standard String](../Topic/How%20to:%20Convert%20System::String%20to%20Standard%20String.md)  
  
-   [How to: Convert Standard String to System::String](../vs140/How-to--Convert-Standard-String-to-System--String.md)  
  
-   [How to: Obtain a Pointer to Byte Array](../vs140/How-to--Obtain-a-Pointer-to-Byte-Array.md)  
  
-   [How to: Load Unmanaged Resources into a Byte Array](../vs140/How-to--Load-Unmanaged-Resources-into-a-Byte-Array.md)  
  
-   [How to: Modify Reference Class in a Native Function](../vs140/How-to--Modify-Reference-Class-in-a-Native-Function.md)  
  
-   [How to: Determine if an Image is Native or CLR](../vs140/How-to--Determine-if-an-Image-is-Native-or-CLR.md)  
  
-   [How to: Add Native DLL to Global Assembly Cache](../vs140/How-to--Add-Native-DLL-to-Global-Assembly-Cache.md)  
  
-   [How to: Hold Reference to Value Type in Native Type](../vs140/How-to--Hold-Reference-to-Value-Type-in-Native-Type.md)  
  
-   [How to: Hold Object Reference in Native Function](../vs140/How-to--Hold-Object-Reference-in-Unmanaged-Memory.md)  
  
-   [How to: Detect /clr Compilation](../vs140/How-to--Detect--clr-Compilation.md)  
  
-   [How to: Convert Between System::Guid and _GUID](../Topic/How%20to:%20Convert%20Between%20System::Guid%20and%20_GUID.md)  
  
-   [How to: Specify an out Parameter](../Topic/How%20to:%20Specify%20an%20out%20Parameter.md)  
  
-   [How to: Use a Native Type in a /clr Compilation](../vs140/How-to--Use-a-Native-Type-in-a--clr-Compilation.md)  
  
-   [How to: Declare Handles in Native Types](../vs140/How-to--Declare-Handles-in-Native-Types.md)  
  
-   [How to: Wrap Native Class for Use by C#](../vs140/How-to--Wrap-Native-Class-for-Use-by-C#.md)  
  
 For information on using delegates in an interop scenario, see [delegate](../vs140/delegate---C---Component-Extensions-.md).  
  
## See Also  
 [Platform Invocation Services](../vs140/Calling-Native-Functions-from-Managed-Code.md)