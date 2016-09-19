---
title: "__property"
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
ms.assetid: 235e3574-6882-4c52-8301-270277b9216d
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# __property
> [!NOTE]
>  This topic applies only to version 1 of Managed Extensions for C++. This syntax should only be used to maintain version 1 code. See [property (Managed Extensions for C++ Programming)](../vs140/property---C---Component-Extensions-.md) for information on using the equivalent functionality in the new syntax.  
  
 Declares either a scalar or indexed property for the managed class.  
  
## Syntax  
  
```  
  
__property function-declarator  
```  
  
## Remarks  
 The `__property` keyword introduces the declaration of a property and can appear in a class, interface, or value type. A property can have a getter function (read only), a setter function (write only), or both (read-write).  
  
> [!NOTE]
>  A property name cannot match the name of the managed class containing it. The return type of the getter function must match the type of the last parameter of a corresponding setter function.  
  
## Example  
 In the following example, a scalar property (`Size`) is added to the `MyClass` declaration. The property is then implicitly set and retrieved using the `get_Size` and `set_Size` functions:  
  
```  
// keyword__property.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc class MyClass {  
public:  
   MyClass() : m_size(0) {}  
   __property int get_Size() { return m_size; }  
   __property void set_Size(int value) { m_size = value; }  
   // compiler generates pseudo data member called Size  
protected:  
   int m_size;  
};  
  
int main() {  
   MyClass* class1 = new MyClass;  
   int curValue;  
  
   Console::WriteLine(class1->Size);  
  
   class1->Size = 4;   // calls the set_Size function with value==4  
   Console::WriteLine(class1->Size);  
  
   curValue = class1->Size;   // calls the get_Size function  
   Console::WriteLine(curValue);  
}  
```  
  
## Output  
  
```  
0  
4  
4  
```