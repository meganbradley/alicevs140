---
title: "safe_cast (C++ Component Extensions)"
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
ms.topic: language-reference
ms.assetid: 4fa688bf-a8ec-49bc-a4c5-f48134efa4f7
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# safe_cast (C++ Component Extensions)
The `safe_cast` operation returns the specified expression as the specified type, if successful; otherwise, throws `InvalidCastException`.  
  
## All Runtimes  
 (There are no remarks for this language feature that apply to all runtimes.)  
  
### Syntax  
  
```cpp  
  
[default]:: safe_cast<  
type-id  
>(  
expression  
)  
  
```  
  
### Parameters  
  
### Remarks  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 `safe_cast` allows you to change the type of a specified expression. In situations where you fully expect a variable or parameter to be convertible to a certain type, you can use safe_cast without a try-catch block to detect programming errors during development. For more information, see [Casting (C++/CX)](http://msdn.microsoft.com/library/windows/apps/hh755802.aspx).  
  
### Syntax  
  
```cpp  
  
[default]:: safe_cast<  
type-id  
>(  
expression  
)  
  
```  
  
### Parameters  
 *type-id*  
 The type to convert *expression* to. A handle to a reference or value type, a value type, or a tracking reference to a reference or value type.  
  
 *expression*  
 An expression that evaluates to a handle to a reference or value type, a value type, or a tracking reference to a reference or value type.  
  
### Remarks  
 `safe_cast` throws `InvalidCastException` if it cannot convert *expression* to the type specified by *type-id*. To catch `InvalidCastException`, specify the [/EHsc](../vs140/-EH--Exception-Handling-Model-.md) compiler option, and use a try/catch statement.  
  
### Requirements  
 Compiler option: **/ZW**  
  
### Examples  
 **Example**  
  
 The following code example demonstrates how to use `safe_cast` with the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
```cpp#  
// safe_cast_ZW.cpp  
// compile with: /ZW /EHsc  
  
using namespace default;  
using namespace Platform;  
  
interface class I1 {};  
interface class I2 {};  
interface class I3 {};  
  
ref class X : public I1, public I2 {};  
  
int main(Array<String^>^ args) {  
   I1^ i1 = ref new X;  
   I2^ i2 = safe_cast<I2^>(i1);   // OK, I1 and I2 have common type: X  
   // I2^ i3 = static_cast<I2^>(i1);   C2440 use safe_cast instead  
   try {  
      I3^ i4 = safe_cast<I3^>(i1);   // Fails because i1 is not derived from I3.  
   }   
   catch(InvalidCastException^ ic) {  
     wprintf(L"Caught expected exception: %s\n", ic->Message);  
   }  
}  
```  
  
 **Output**  
  
 **Caught expected exception: InvalidCastException**   
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 `safe_cast` allows you to change the type of an expression and generate verifiable MSIL code.  
  
### Syntax  
  
```cpp  
  
[cli]:: safe_cast<  
type-id  
>(  
expression  
)  
  
```  
  
### Parameters  
 *type-id*  
 A handle to a reference or value type, a value type, or a tracking reference to a reference or value type.  
  
 *expression*  
 An expression that evaluates to a handle to a reference or value type, a value type, or a tracking reference to a reference or value type.  
  
### Remarks  
 The expression `safe_cast<`*type-id*`>(`*expression*`)` converts the operand expression to an object of type type-id.  
  
 The compiler will accept a [static_cast](../vs140/static_cast-Operator.md) in most places that it will accept a `safe_cast`.  However, `safe_cast` is guaranteed to produce verifiable MSIL, where as a `static_cast` could produce unverifiable MSIL.  See [Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md) and [PEVerify Tool (Peverify.exe)](assetId:///f4f46f9e-8d08-4e66-a94b-0c69c9b0bbfa) for more information on verifiable code.  
  
 Like `static_cast`, `safe_cast` invokes user-defined conversions.  
  
 For more information about casts, see [Casting Operators](../vs140/Casting-Operators.md).  
  
 `safe_cast` does not apply a **const_cast** (cast away **const**).  
  
 `safe_cast` is in the cli namespace.  See [cli Namespace](../vs140/Platform--default--and-cli-Namespaces---C---Component-Extensions-.md) for more information.  
  
 For more information on **safe_cas**t, see:  
  
-   [C-Style Casts with /clr](../vs140/C-Style-Casts-with--clr--C---CLI-.md)  
  
-   [How to: Upcast with safe_cast](../Topic/How%20to:%20Use%20safe_cast%20in%20C++-CLI.md)  
  
-   [How to: Downcast with safe_cast](../vs140/How-to--Downcast-with-safe_cast.md)  
  
-   [How to: Using safe_cast and Generic Types](../vs140/How-to--Use-safe_cast-and-Generic-Types.md)  
  
-   [How to: Use safe_cast and User-Defined Conversions](../vs140/How-to--Use-safe_cast-and-User-Defined-Conversions.md)  
  
-   [How to: Use safe_cast and Boxing](../vs140/How-to--Use-safe_cast-and-Boxing.md)  
  
-   [How to: Use safe_cast and Unboxing](../vs140/How-to--Use-safe_cast-and-Unboxing.md)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 One example of where the compiler will not accept a `static_cast` but will accept a `safe_cast` is for casts between unrelated interface types.  With `safe_cast`, the compiler will not issue a conversion error and will perform a check at runtime to see if the cast is possible  
  
```cpp  
// safe_cast.cpp  
// compile with: /clr  
using namespace System;  
  
interface class I1 {};  
interface class I2 {};  
interface class I3 {};  
  
ref class X : public I1, public I2 {};  
  
int main() {  
   I1^ i1 = gcnew X;  
   I2^ i2 = safe_cast<I2^>(i1);   // OK, I1 and I2 have common type: X  
   // I2^ i3 = static_cast<I2^>(i1);   C2440 use safe_cast instead  
   try {  
      I3^ i4 = safe_cast<I3^>(i1);   // fail at runtime, no common type  
   }   
   catch(InvalidCastException^) {  
      Console::WriteLine("Caught expected exception");  
   }  
}  
```  
  
 **Output**  
  
 **Caught expected exception**   
## See Also  
 [Component Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)