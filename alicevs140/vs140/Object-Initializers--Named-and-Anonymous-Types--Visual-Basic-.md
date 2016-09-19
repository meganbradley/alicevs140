---
title: "Object Initializers: Named and Anonymous Types (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2df3807-a70f-49dd-ac94-f1e07f472b1b
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Object Initializers: Named and Anonymous Types (Visual Basic)
Object initializers enable you to specify properties for a complex object by using a single expression. They can be used to create instances of named types and of anonymous types.  
  
## Declarations  
 Declarations of instances of named and anonymous types can look almost identical, but their effects are not the same. Each category has abilities and restrictions of its own. The following example shows a convenient way to declare and initialize an instance of a named class, `Customer`, by using an object initializer list. Notice that the name of the class is specified after the keyword `New`.  
  
 [!CODE [VbVbalrObjectInit#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#1)]  
  
 An anonymous type has no usable name. Therefore an instantiation of an anonymous type cannot include a class name.  
  
 [!CODE [VbVbalrObjectInit#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#2)]  
  
 The requirements and results of the two declarations are not the same. For `namedCust`, a `Customer` class that has a `Name` property must already exist, and the declaration creates an instance of that class. For `anonymousCust`, the compiler defines a new class that has one property, a string called `Name`, and creates a new instance of that class.  
  
## Named Types  
 Object initializers provide a simple way to call the constructor of a type and then set the values of some or all properties in a single statement. The compiler invokes the appropriate constructor for the statement: the default constructor if no arguments are presented, or a parameterized constructor if one or more arguments are sent. After that, the specified properties are initialized in the order in which they are presented in the initializer list.  
  
 Each initialization in the initializer list consists of the assignment of an initial value to a member of the class. The names and data types of the members are determined when the class is defined. In the following examples, the `Customer` class must exist, and must have members named `Name` and `City` that can accept string values.  
  
 [!CODE [VbVbalrObjectInit#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#3)]  
  
 Alternatively, you can obtain the same result by using the following code:  
  
 [!CODE [VbVbalrObjectInit#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#4)]  
  
 Each of these declarations is equivalent to the following example, which creates a `Customer` object by using the default constructor, and then specifies initial values for the `Name` and `City` properties by using a `With` statement.  
  
 [!CODE [VbVbalrObjectInit#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#5)]  
  
 If the `Customer` class contains a parameterized constructor that enables you to send in a value for `Name`, for example, you can also declare and initialize a `Customer` object in the following ways:  
  
 [!CODE [VbVbalrObjectInit#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#6)]  
  
 You do not have to initialize all properties, as the following code shows.  
  
 [!CODE [VbVbalrObjectInit#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#7)]  
  
 However, the initialization list cannot be empty. Uninitialized properties retain their default values.  
  
### Type Inference with Named Types  
 You can shorten the code for the declaration of `cust1` by combining object initializers and local type inference. This enables you to omit the `As` clause in the variable declaration. The data type of the variable is inferred from the type of the object that is created by the assignment. In the following example, the type of `cust6` is `Customer`.  
  
 [!CODE [VbVbalrObjectInit#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#8)]  
  
### Remarks About Named Types  
  
-   A class member cannot be initialized more than one time in the object initializer list. The declaration of `cust7` causes an error.  
  
     [!CODE [VbVbalrObjectInit#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#9)]  
  
-   A member can be used to initialize itself or another field. If a member is accessed before it has been initialized, as in the following declaration for `cust8`, the default value will be used. Remember that when a declaration that uses an object initializer is processed, the first thing that happens is that the appropriate constructor is invoked. After that, the individual fields in the initializer list are initialized. In the following examples, the default value for `Name` is assigned for `cust8`, and an initialized value is assigned in `cust9`.  
  
     [!CODE [VbVbalrObjectInit#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#10)]  
  
     The following example uses the parameterized constructor from `cust3` and `cust4` to declare and initialize `cust10` and `cust11`.  
  
     [!CODE [VbVbalrObjectInit#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#11)]  
  
-   Object initializers can be nested. In the following example, `AddressClass` is a class that has two properties, `City` and `State`, and the `Customer` class has an `Address` property that is an instance of `AddressClass`.  
  
     [!CODE [VbVbalrObjectInit#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#12)]  
  
-   The initialization list cannot be empty.  
  
-   The instance being initialized cannot be of type Object.  
  
-   Class members being initialized cannot be shared members, read-only members, constants, or method calls.  
  
-   Class members being initialized cannot be indexed or qualified. The following examples raise compiler errors:  
  
     `'' Not valid.`  
  
     `' Dim c1 = New Customer With {.OrderNumbers(0) = 148662}`  
  
     `' Dim c2 = New Customer with {.Address.City = "Springfield"}`  
  
## Anonymous Types  
 Anonymous types use object initializers to create instances of new types that you do not explicitly define and name. Instead, the compiler generates a type according to the properties you designate in the object initializer list. Because the name of the type is not specified, it is referred to as an *anonymous type*. For example, compare the following declaration to the earlier one for `cust6`.  
  
 [!CODE [VbVbalrObjectInit#13](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#13)]  
  
 The only difference syntactically is that no name is specified after `New` for the data type. However, what happens is quite different. The compiler defines a new anonymous type that has two properties, `Name` and `City`, and creates an instance of it with the specified values. Type inference determines the types of `Name` and `City` in the example to be strings.  
  
> [!CAUTION]
>  The name of the anonymous type is generated by the compiler, and may vary from compilation to compilation. Your code should not use or rely on the name of an anonymous type.  
  
 Because the name of the type is not available, you cannot use an `As` clause to declare `cust13`. Its type must be inferred. Without using late binding, this limits the use of anonymous types to local variables.  
  
 Anonymous types provide critical support for [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries. For more information about the use of anonymous types in queries, see [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md) and [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md).  
  
### Remarks About Anonymous Types  
  
-   Typically, all or most of the properties in an anonymous type declaration will be key properties, which are indicated by typing the keyword `Key` in front of the property name.  
  
     [!CODE [VbVbalrObjectInit#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#14)]  
  
     For more information about key properties, see [Key](../Topic/Key%20\(Visual%20Basic\).md).  
  
-   Like named types, initializer lists for anonymous type definitions must declare at least one property.  
  
     [!CODE [VbVbalrObjectInit#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#2)]  
  
-   When an instance of an anonymous type is declared, the compiler generates a matching anonymous type definition. The names and data types of the properties are taken from the instance declaration, and are included by the compiler in the definition. The properties are not named and defined in advance, as they would be for a named type. Their types are inferred. You cannot specify the data types of the properties by using an `As` clause.  
  
-   Anonymous types can also establish the names and values of their properties in several other ways. For example, an anonymous type property can take both the name and the value of a variable, or the name and value of a property of another object.  
  
     [!CODE [VbVbalrObjectInit#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#15)]  
  
     For more information about the options for defining properties in anonymous types, see [How to: Infer Property Names and Types in Anonymous Types](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md).  
  
## See Also  
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)   
 [Anonymous types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [How to: Infer Property Names and Types in Anonymous Types](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md)   
 [Key](../Topic/Key%20\(Visual%20Basic\).md)   
 [How to: Declare an Object by Using an Object Initializer](../vs140/How-to--Declare-an-Object-by-Using-an-Object-Initializer--Visual-Basic-.md)