---
title: "Windows Runtime and Managed Templates (C++ Component Extensions)"
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
ms.assetid: cf59d16b-5514-448b-9a95-e0b4fcb616a6
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Runtime and Managed Templates (C++ Component Extensions)
Templates enable you to define a prototype of a Windows Runtime or common language runtime type, and then instantiate variations of that type by using different template type parameters.  
  
## All Runtimes  
 You can create templates from value or reference types.  For more information about creating value or reference types, see [Classes and Structs (Managed)](../vs140/Classes-and-Structs---C---Component-Extensions-.md).  
  
 For more information about standard C++ class templates, see [Class Templates](../vs140/Class-Templates.md).  
  
## Windows Runtime  
 (There are no remarks for this language feature that apply to only the Windows Runtime.)  
  
### Requirements  
 Compiler option: **/ZW**  
  
## Common Language Runtime  
 There are some limitations to creating class templates from managed types, which are demonstrated in the following code examples.  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 It is possible to instantiate a generic type with a managed type template parameter, but you cannot instantiate a managed template with a generic type template parameter.  This is because generic types are resolved at runtime.  For more information, see [Generics and Templates](../vs140/Generics-and-Templates--Visual-C---.md).  
  
```cpp  
// managed_templates.cpp  
// compile with: /clr /c  
  
generic<class T>   
ref class R;   
  
template<class T>   
ref class Z {  
   // Instantiate a generic with a template parameter.  
   R<T>^ r;    // OK  
};  
  
generic<class T>   
ref class R {  
   // Cannot instantiate a template with a generic parameter.  
   Z<T>^ z;   // C3231  
};  
```  
  
 **Example**  
  
 A generic type or function cannot be nested in a managed template.  
  
```cpp  
// managed_templates_2.cpp  
// compile with: /clr /c  
  
template<class T> public ref class R {  
   generic<class T> ref class W {};   // C2959  
};  
```  
  
 **Example**  
  
 You cannot access templates defined in a referenced assembly with C++/CLI language syntax, but you can use reflection.  If a template is not instantiated, it’s not emitted in the metadata.  If a template is instantiated, only referenced member functions will appear in metadata.  
  
```cpp  
// managed_templates_3.cpp  
// compile with: /clr  
  
// Will not appear in metadata.  
template<class T> public ref class A {};  
  
// Will appear in metadata as a specialized type.  
template<class T> public ref class R {  
public:  
   // Test is referenced, will appear in metadata  
   void Test() {}  
  
   // Test2 is not referenced, will not appear in metadata  
   void Test2() {}  
};  
  
// Will appear in metadata.  
generic<class T> public ref class G { };  
  
public ref class S { };  
  
int main() {  
   R<int>^ r = gcnew R<int>;  
   r->Test();  
}  
```  
  
 **Example**  
  
 You can change the managed modifier of a class in a partial specialization or explicit specialization of a class template.  
  
```cpp  
// managed_templates_4.cpp  
// compile with: /clr /c  
  
// class template  
// ref class  
template <class T>  
ref class A {};  
  
// partial template specialization  
// value type  
template <class T>  
value class A <T *> {};  
  
// partial template specialization  
// interface  
template <class T>   
interface class A<T%> {};  
  
// explicit template specialization  
// native class  
template <>  
class A <int> {};  
  
```  
  
## See Also  
 [Component Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)