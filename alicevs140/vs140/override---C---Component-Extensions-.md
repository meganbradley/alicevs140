---
title: "override  (C++ Component Extensions)"
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
ms.assetid: 34d19257-1686-4fcd-96f5-af07c70ba914
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# override  (C++ Component Extensions)
The `override` context-sensitive keyword indicates that a member of a type overrides a base class or a base interface member.  
  
## Remarks  
 The `override` keyword is valid when compiling for native targets (default compiler option), Windows Runtime targets (**/ZW** compiler option), or common language runtime targets (**/clr** compiler option).  
  
 For more information about override specifiers, see [override Specifier](../vs140/override-Specifier.md) and [Override Specifiers and Native Compilations](../vs140/How-to--Declare-Override-Specifiers-in-Native-Compilations--C---CLI-.md).  
  
 For more information about context-sensitive keywords, see [Context-Sensitive Keywords](../vs140/Context-Sensitive-Keywords---C---Component-Extensions-.md).  
  
## Examples  
 **Example**  
  
 The following code example shows that `override` can also be used in native compilations.  
  
```cpp#  
// override_keyword_1.cpp  
// compile with: /c  
struct I1 {  
   virtual void f();  
};  
  
struct X : public I1 {  
   virtual void f() override {}  
};  
```  
  
 **Example**  
  
 The following code example shows that `override` can be used in Windows Runtime compilations.  
  
```cpp#  
// override_keyword_2.cpp  
// compile with: /ZW /c  
ref struct I1 {  
   virtual void f();  
};  
  
ref struct X : public I1 {  
   virtual void f() override {}  
};  
```  
  
 **Requirements**  
  
 Compiler option: **/ZW**  
  
 **Example**  
  
 The following code example shows that `override` can be used in common language runtime compilations.  
  
```cpp#  
// override_keyword_3.cpp  
// compile with: /clr /c  
ref struct I1 {  
   virtual void f();  
};  
  
ref struct X : public I1 {  
   virtual void f() override {}  
};  
```  
  
 **Requirements**  
  
 Compiler option: **/clr**  
  
## See Also  
 [override Specifier](../vs140/override-Specifier.md)   
 [Override Specifiers](../vs140/Override-Specifiers---C---Component-Extensions-.md)