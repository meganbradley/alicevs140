---
title: "Auto-Implemented Properties (Visual Basic)"
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
ms.assetid: 5c669f0b-cf95-4b4e-ae84-9cc55212ca87
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Auto-Implemented Properties (Visual Basic)
*Auto-implemented properties* enable you to quickly specify a property of a class without having to write code to `Get` and `Set` the property. When you write code for an auto-implemented property, the Visual Basic compiler automatically creates a private field to store the property variable in addition to creating the associated `Get` and `Set` procedures.  
  
 With auto-implemented properties, a property, including a default value, can be declared in a single line. The following example shows three property declarations.  
  
 [!CODE [VbVbalrAutoImplementedProperties#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrautoimplementedproperties#1)]  
  
 An auto-implemented property is equivalent to a property for which the property value is stored in a private field. The following code example shows an auto-implemented property.  
  
 [!CODE [VbVbalrAutoImplementedProperties#5](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrautoimplementedproperties#5)]  
  
 The following code example shows the equivalent code for the previous auto-implemented property example.  
  
 [!CODE [VbVbalrAutoImplementedProperties#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrautoimplementedproperties#2)]  
  
 The following code show implementing readonly properties:  
  
```vb  
Class Customer  
   Public ReadOnly Property Tags As New List(Of String)  
   Public ReadOnly Property Name As String = ""  
   Public ReadOnly Property File As String  
  
   Sub New(file As String)  
      Me.File = file  
   End Sub  
End Class  
  
```  
  
 You can assign to the property with initialization expressions as shown in the example, or you can assign to the properties in the containing type’s constructor.  You can assign to the backing fields of readonly properties at any time.  
  
## Backing Field  
 When you declare an auto-implemented property, Visual Basic automatically creates a hidden private field called the *backing field* to contain the property value. The backing field name is the auto-implemented property name preceded by an underscore (_). For example, if you declare an auto-implemented property named `ID`, the backing field is named `_ID`. If you include a member of your class that is also named `_ID`, you produce a naming conflict and Visual Basic reports a compiler error.  
  
 The backing field also has the following characteristics:  
  
-   The access modifier for the backing field is always `Private`, even when the property itself has a different access level, such as `Public`.  
  
-   If the property is marked as `Shared`, the backing field also is shared.  
  
-   Attributes specified for the property do not apply to the backing field.  
  
-   The backing field can be accessed from code within the class and from debugging tools such as the Watch window. However, the backing field does not show in an IntelliSense word completion list.  
  
## Initializing an Auto-Implemented Property  
 Any expression that can be used to initialize a field is valid for initializing an auto-implemented property. When you initialize an auto-implemented property, the expression is evaluated and passed to the `Set` procedure for the property. The following code examples show some auto-implemented properties that include initial values.  
  
 [!CODE [VbVbalrAutoImplementedProperties#3](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrautoimplementedproperties#3)]  
  
 You cannot initialize an auto-implemented property that is a member of an `Interface`, or one that is marked `MustOverride`.  
  
 When you declare an auto-implemented property as a member of a `Structure`, you can only initialize the auto-implemented property if it is marked as `Shared`.  
  
 When you declare an auto-implemented property as an array, you cannot specify explicit array bounds. However, you can supply a value by using an array initializer, as shown in the following examples.  
  
 [!CODE [VbVbalrAutoImplementedProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrautoimplementedproperties#4)]  
  
## Property Definitions That Require Standard Syntax  
 Auto-implemented properties are convenient and support many programming scenarios. However, there are situations in which you cannot use an auto-implemented property and must instead use standard, or *expanded*, property syntax.  
  
 You have to use expanded property-definition syntax if you want to do any one of the following:  
  
-   Add code to the `Get` or `Set` procedure of a property, such as code to validate incoming values in the `Set` procedure. For example, you might want to verify that a string that represents a telephone number contains the required number of numerals before setting the property value.  
  
-   Specify different accessibility for the `Get` and `Set` procedure. For example, you might want to make the `Set` procedure `Private` and the `Get` procedure `Public`.  
  
-   Create properties that are `WriteOnly`.  
  
-   Use parameterized properties (including `Default` properties). You must declare an expanded property in order to specify a parameter for the property, or to specify additional parameters for the `Set` procedure.  
  
-   Place an attribute on the backing field, or change the access level of the backing field.  
  
-   Provide XML comments for the backing field.  
  
## Expanding an Auto-Implemented Property  
 If you have to convert an auto-implemented property to an expanded property that contains a `Get` or `Set` procedure, the Visual Basic Code Editor can automatically generate the `Get` and `Set` procedures and `End Property` statement for the property. The code is generated if you put the cursor on a blank line following the `Property` statement, type a `G` (for `Get`) or an `S` (for `Set`) and press ENTER. The Visual Basic Code Editor automatically generates the `Get` or `Set` procedure for read-only and write-only properties when you press ENTER at the end of a `Property` statement.  
  
## See Also  
 [How to: Declare and Call a Default Property in Visual Basic](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md)   
 [WriteOnly](../vs140/WriteOnly--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)