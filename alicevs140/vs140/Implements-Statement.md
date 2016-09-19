---
title: "Implements Statement"
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
ms.assetid: 1fafb83f-f55a-4215-8ea9-681e8622613d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implements Statement
Specifies one or more interfaces, or interface members, that must be implemented in the class or structure definition in which it appears.  
  
## Syntax  
  
```  
Implements interfacename [, ...]  
-or-  
Implements interfacename.interfacemember [, ...]  
```  
  
## Parts  
 `interfacename`  
 Required. An interface whose properties, procedures, and events are to be implemented by corresponding members in the class or structure.  
  
 `interfacemember`  
 Required. The member of an interface that is being implemented.  
  
## Remarks  
 An interface is a collection of prototypes representing the members (properties, procedures, and events) the interface encapsulates. Interfaces contain only the declarations for members; classes and structures implement these members. For more information, see [Interfaces (Visual Basic)](../vs140/Interfaces--Visual-Basic-.md).  
  
 The `Implements` statement must immediately follow the `Class` or `Structure` statement.  
  
 When you implement an interface, you must implement all the members declared in the interface. Omitting any member is considered to be a syntax error. To implement an individual member, you specify the [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md) keyword (which is separate from the `Implements` statement) when you declare the member in the class or structure. For more information, see [Interfaces](../vs140/Interfaces--Visual-Basic-.md).  
  
 Classes can use [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md) implementations of properties and procedures, but these members are accessible only by casting an instance of the implementing class into a variable declared to be of the type of the interface.  
  
## Example  
 The following example shows how to use the `Implements` statement to implement members of an interface. It defines an interface named `ICustomerInfo` with an event, a property, and a procedure. The class `customerInfo` implements all the members defined in the interface.  
  
 [!CODE [VbVbalrStatements#33](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#33)]  
  
 Note that the class `customerInfo` uses the `Implements` statement on a separate source code line to indicate that the class implements all the members of the `ICustomerInfo` interface. Then each member in the class uses the `Implements` keyword as part of its member declaration to indicate that it implements that interface member.  
  
## Example  
 The following two procedures show how you could use the interface implemented in the preceding example. To test the implementation, add these procedures to your project and call the `testImplements` procedure.  
  
 [!CODE [VbVbalrStatements#34](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#34)]  
  
## See Also  
 [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md)   
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Interfaces](../vs140/Interfaces--Visual-Basic-.md)