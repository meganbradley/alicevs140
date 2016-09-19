---
title: "property  (C++ Component Extensions)"
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
ms.assetid: cc79d2b2-f013-4d81-8252-eece97a18704
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# property  (C++ Component Extensions)
Declares a *property*, which is a member function that behaves and is accessed like a data member or an array element.  
  
## All Runtimes  
 You can declare one of the following types of properties.  
  
 *simple property*  
 By default, creates a *set accessor* that assigns the property value, a *get accessor* that retrieves the property value, and a compiler-generated private data member that contains the property value.  
  
 *property block*  
 Use this to create user-defined get and/or set accessors. The property is read/write if both the get and set accessors are defined, read-only if only the get accessor is defined, and write-only if only the set accessor is defined.  
  
 You must explicitly declare a data member to contain the property value.  
  
 *indexed property*  
 A property block that you can use to get and set a property value that is specified by one or more indexes.  
  
 You can create an indexed property that has either a user-defined property name or a *default* property name. The name of a default index property is the name of the class in which the property is defined. To declare a default property, specify the `default` keyword instead of a property name.  
  
 You must explicitly declare a data member to contain the property value. For an indexed property, the data member is typically an array or a collection.  
  
### Syntax  
  
```cpp  
  
   property  
   type  
   property_name;  
  
propertytypeproperty_name{access-modifiertypeget()inheritance-modifier{property_body};access-modifiervoid set(typevalue)inheritance-modifier{property_body};  
}propertytypeproperty_name[index_list] {access-modifiertypeget(index_list)inheritance-modifier{property_body};access-modifiervoid set(index_list, value)inheritance-modifier{property_body};  
}propertytypedefault[index_list] {access-modifiertypeget(index_list)inheritance-modifier {property_body};  
   access-modifiervoid set(index_list, value)inheritance-modifier{property_body};  
}  
```  
  
### Parameters  
 `type`  
 The data type of the property value, and consequently the property itself.  
  
 `property_name`  
 The name of the property.  
  
 `access-modifier`  
 An access qualifier. Valid qualifiers are `static` and `virtual`.  
  
 The get or set accessors need not agree on the `virtual` qualifier, but they must agree on the `static` qualifier.  
  
 `inheritance-modifier`  
 An inheritance qualifier. Valid qualifiers are `abstract` and `sealed`.  
  
 `index_list`  
 A comma-delimited list of one or more indexes. Each index consists of an index type, and an optional identifier that can be used in the property method body.  
  
 `value`  
 The value to assign to the property in a set operation, or retrieve in a get operation.  
  
 `property_body`  
 The property method body of the set or get accessor. The `property_body` can use the `index_list` to access the underlying property data member, or as parameters in user-defined processing.  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 For more information, see [Properties (C++/CX)](http://msdn.microsoft.com/library/windows/apps/hh755807.aspx).  
  
### Requirements  
 Compiler option: **/ZW**  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 **Syntax**  
  
```  
  
      modifier  
      property  
      type  
      property_name;  
  
modifierpropertytypeproperty_name {  
   modifier void set(type);  
   modifiertypeget();  
}  
modifierpropertytypeproperty_name[index-list, value] {  
   modifier void set(index-list, value);  
   modifiertypeget(index-list);  
  
modifierpropertytypedefault[index];  
}  
```  
  
 **Parameters**  
  
 *modifier*  
 A modifier that can be used on either a property declaration or a get/set accessor method. Possible values are `static` and `virtual`.  
  
 *type*  
 The type of the value that is represented by the property.  
  
 *property_name*  
 Parameter(s) for the raise method; must match the signature of the delegate.  
  
 *index_list*  
 A comma-delimited list of one or more indexes, specified in square brackets (the subscript operator, ([])). For each index, specify a type and optionally an identifier that can be used in the property method body.  
  
 **Remarks**  
  
 The first syntax example shows a *simple property*, which implicitly declares both a `set` and `get` method. The compiler automatically creates a private field to store the value of the property.  
  
 The second syntax example shows a *property block*, which explicitly declares both a `set` and `get` method.  
  
 The third syntax example shows a customer-defined *index property*. An index property takes parameters in addition to the value to be set or retrieved. You must specify a name for the property. Unlike a simple property, the `set` and/or `get` methods of an index property must be explicitly defined, and you must specify a name for the property.  
  
 The fourth syntax example shows a *default* property, which provides array-like access to an instance of the type. The keyword, `default`, serves only to specify a default property. The name of the default property is the name of the type in which the property is defined.  
  
 The `property` keyword can appear in a class, interface, or value type. A property can have a get function (read-only), a set function (write-only), or both (read-write).  
  
 A property name cannot match the name of the managed class that contains it. The return type of the getter function must match the type of the last parameter of a corresponding setter function.  
  
 To client code, a property has the appearance of an ordinary data member, and can be written to or read from by using the same syntax as a data member.  
  
 The get and set methods need not agree on the `virtual` modifier.  
  
 The accessibility of the get and set method can differ.  
  
 The definition of a property method can appear outside the class body, just like an ordinary method.  
  
 The get and the set method for a property shall agree on the **static** modifier.  
  
 A property is scalar if its get and set methods fit the following description:  
  
-   The get method has no parameters, and has return type `T`.  
  
-   The set method has a parameter of type `T`, and return type **void**.  
  
 There shall be only one scalar property declared in a scope with the same identifier. Scalar properties cannot be overloaded.  
  
 When a property data member is declared, the compiler injects a data member—sometimes referred to as the "backing store"—in the class. However, the name of the data member is of a form such that you cannot reference the member in the source as if it were an actual data member of the containing class. Use ildasm.exe to view the metadata for your type and see the compiler-generated name for the property's backing store.  
  
 Different accessibility is allowed for the accessor methods in a property block.  That is, the set method can be public and the get method can be private.  However, it is an error for an accessor method to have a less restrictive accessibility than what is on the declaration of the property itself.  
  
 `property` is a context-sensitive keyword.  For more information, see [Context-Sensitive Keywords](../vs140/Context-Sensitive-Keywords---C---Component-Extensions-.md).  
  
 For more information about properties, see  
  
-   [Indexed Properties](../vs140/How-to--Use-Indexed-Properties.md)  
  
-   [Static Properties](../vs140/How-to--Declare-and-Use-Static-Properties.md)  
  
-   [Virtual Properties](../vs140/How-to--Declare-and-Use-Virtual-Properties.md)  
  
-   [Multidimensional Properties](../vs140/How-to--Use-Multidimensional-Properties.md)  
  
-   [Overloading Property Accessor Methods](../vs140/How-to--Overload-Property-Accessor-Methods.md)  
  
-   [How to: Declare Abstract and Sealed Properties](../vs140/How-to--Declare-Abstract-and-Sealed-Properties.md)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 The following example shows the declaration and use of a property data member and a property block.  It also shows that a property accessor can be defined out of class.  
  
```  
// mcppv2_property.cpp  
// compile with: /clr  
using namespace System;  
public ref class C {  
   int MyInt;  
public:  
  
   // property data member  
   property String ^ Simple_Property;  
  
   // property block  
   property int Property_Block {  
  
      int get();  
  
      void set(int value) {  
         MyInt = value;  
      }  
   }  
};  
  
int C::Property_Block::get() {  
   return MyInt;  
}  
  
int main() {  
   C ^ MyC = gcnew C();  
   MyC->Simple_Property = "test";  
   Console::WriteLine(MyC->Simple_Property);  
  
   MyC->Property_Block = 21;  
   Console::WriteLine(MyC->Property_Block);  
}  
```  
  
 **Output**  
  
 **test**   
 **21**   
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)