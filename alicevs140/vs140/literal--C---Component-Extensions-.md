---
title: "literal (C++ Component Extensions)"
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
ms.assetid: 6b1a1f36-2e1d-4a23-8eb6-172f4f3c477f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# literal (C++ Component Extensions)
A variable (data member) marked as `literal` in a **/clr** compilation is the native equivalent of a `static const` variable.  
  
## All Platforms  
 **Remarks**  
  
 (There are no remarks for this language feature that apply to all runtimes.)  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 **Remarks**  
  
 (There are no remarks for this language feature that apply to only the Windows Runtime.)  
  
### Requirements  
 Compiler option: **/ZW**  
  
## Common Language Runtime  
  
## Remarks  
 A data member marked as `literal`must be initialized when declared and the value must be a constant integral, enum, or string type. Conversion from the type of the initialization expression to the type of the static const data-member must not require a user-defined conversion.  
  
 No memory is allocated for the literal field at runtime; the compiler only inserts its value in the metadata for the class.  
  
 A variable marked `static const` will not be available in metadata to other compilers.  
  
 For more information, see [static (C++)](../vs140/Static--C---.md) and [const (C++)](../vs140/const--C---.md).  
  
 `literal` is a context-sensitive keyword. See [Context-Sensitive Keywords](../vs140/Context-Sensitive-Keywords---C---Component-Extensions-.md) for more information.  
  
## Example  
 This example shows that a `literal` variable implies `static`.  
  
```  
// mcppv2_literal.cpp  
// compile with: /clr  
ref struct X {  
   literal int i = 4;  
};  
  
int main() {  
   int value = X::i;  
}  
```  
  
## Example  
 The following sample shows the affect of literal in metadata:  
  
```  
// mcppv2_literal2.cpp  
// compile with: /clr /LD  
public ref struct A {  
   literal int lit = 0;  
   static const int sc = 1;  
};  
```  
  
 Notice the difference in the metadata for `sc` and `lit`: the `modopt` directive is applied to `sc`, meaning it can be ignored by other compilers.  
  
```  
.field public static int32 modopt([mscorlib]System.Runtime.CompilerServices.IsConst) sc = int32(0x0000000A)  
```  
  
```  
.field public static literal int32 lit = int32(0x0000000A)  
```  
  
## Example  
 The following sample, authored in C#, references the metadata created in the previous sample and shows the affect of `literal` and `static const` variables:  
  
```  
// mcppv2_literal3.cs  
// compile with: /reference:mcppv2_literal2.dll  
// A C# program  
class B {  
   public static void Main() {  
      // OK  
      System.Console.WriteLine(A.lit);  
      System.Console.WriteLine(A.sc);  
  
      // C# does not enforce C++ const  
      A.sc = 9;  
      System.Console.WriteLine(A.sc);  
  
      // C# enforces const for a literal  
      A.lit = 9;   // CS0131  
  
      // you can assign a C++ literal variable to a C# const variable  
      const int i = A.lit;  
      System.Console.WriteLine(i);  
  
      // but you cannot assign a C++ static const variable  
      // to a C# const variable  
      const int j = A.sc;   // CS0133  
      System.Console.WriteLine(j);  
   }  
}  
```  
  
## Requirements  
 Compiler option: **/clr**  
  
## See Also  
 [Component Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)