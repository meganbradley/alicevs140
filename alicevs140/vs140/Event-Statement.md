---
title: "Event Statement"
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
ms.assetid: 306ff8ed-74dd-4b6a-bd2f-e91b17474042
caps.latest.revision: 35
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event Statement
Declares a user-defined event.  
  
## Syntax  
  
```  
[ <attrlist> ] [ accessmodifier ] _  
[ Shared ] [ Shadows ] Event eventname[(parameterlist)] _  
[ Implements implementslist ]  
' -or-  
[ <attrlist> ] [ accessmodifier ] _  
[ Shared ] [ Shadows ] Event eventname As delegatename _  
[ Implements implementslist ]  
' -or-  
 [ <attrlist> ] [ accessmodifier ] _  
[ Shared ] [ Shadows ] Custom Event eventname As delegatename _  
[ Implements implementslist ]  
   [ <attrlist> ] AddHandler(ByVal value As delegatename)  
      [ statements ]  
   End AddHandler  
   [ <attrlist> ] RemoveHandler(ByVal value As delegatename)  
      [ statements ]  
   End RemoveHandler  
   [ <attrlist> ] RaiseEvent(delegatesignature)  
      [ statements ]  
   End RaiseEvent  
End Event  
```  
  
## Parts  
  
|||  
|-|-|  
|Part|Description|  
|`attrlist`|Optional. List of attributes that apply to this event. Multiple attributes are separated by commas. You must enclose the [Attribute List](../vs140/Attribute-List--Visual-Basic-.md) in angle brackets ("`<`" and "`>`").|  
|`accessmodifier`|Optional. Specifies what code can access the event. Can be one of the following:<br /><br /> -   [Public](../vs140/Public--Visual-Basic-.md)—any code that can access the element that declares it can access it.<br />-   [Protected](../vs140/Protected--Visual-Basic-.md)—only code within its class or a derived class can access it.<br />-   [Friend](../Topic/Friend%20\(Visual%20Basic\).md)—only code in the same assembly can access it.<br />-   [Private](../vs140/Private--Visual-Basic-.md)—only code in the element that declares it can access it.<br /><br /> You can specify `Protected Friend` to enable access from code in the event's class, a derived class, or the same assembly.|  
|`Shared`|Optional. Specifies that this event is not associated with a specific instance of a class or structure.|  
|`Shadows`|Optional. Indicates that this event redeclares and hides an identically named programming element, or set of overloaded elements, in a base class. You can shadow any kind of declared element with any other kind.<br /><br /> A shadowed element is unavailable from within the derived class that shadows it, except from where the shadowing element is inaccessible. For example, if a `Private` element shadows a base-class element, code that does not have permission to access the `Private` element accesses the base-class element instead.|  
|`eventname`|Required. Name of the event; follows standard variable naming conventions.|  
|`parameterlist`|Optional. List of local variables that represent the parameters of this event. You must enclose the [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md) in parentheses.|  
|`Implements`|Optional. Indicates that this event implements an event of an interface.|  
|`implementslist`|Required if `Implements` is supplied. List of `Sub` procedures being implemented. Multiple procedures are separated by commas:<br /><br /> *implementedprocedure* [ , *implementedprocedure* ... ]<br /><br /> Each `implementedprocedure` has the following syntax and parts:<br /><br /> `interface`.`definedname`<br /><br /> -   `interface` - Required. Name of an interface that this procedure's containing class or structure is implementing.<br />-   `Definedname` - Required. Name by which the procedure is defined in `interface`. This does not have to be the same as `name`, the name that this procedure is using to implement the defined procedure.|  
|`Custom`|Required. Events declared as `Custom` must define custom `AddHandler`, `RemoveHandler`, and `RaiseEvent` accessors.|  
|`delegatename`|Optional. The name of a delegate that specifies the event-handler signature.|  
|`AddHandler`|Required. Declares an `AddHandler` accessor, which specifies the statements to execute when an event handler is added, either explicitly by using the `AddHandler` statement or implicitly by using the `Handles` clause.|  
|`End AddHandler`|Required. Terminates the `AddHandler` block.|  
|`value`|Required. Parameter name.|  
|`RemoveHandler`|Required. Declares a `RemoveHandler` accessor, which specifies the statements to execute when an event handler is removed using the `RemoveHandler` statement.|  
|`End RemoveHandler`|Required. Terminates the `RemoveHandler` block.|  
|`RaiseEvent`|Required. Declares a `RaiseEvent` accessor, which specifies the statements to execute when the event is raised using the `RaiseEvent` statement. Typically, this invokes a list of delegates maintained by the `AddHandler` and `RemoveHandler` accessors.|  
|`End RaiseEvent`|Required. Terminates the `RaiseEvent` block.|  
|`delegatesignature`|Required. List of parameters that matches the parameters required by the `delegatename` delegate. You must enclose the [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md) in parentheses.|  
|`statements`|Optional. Statements that contain the bodies of the `AddHandler`, `RemoveHandler`, and `RaiseEvent` methods.|  
|`End Event`|Required. Terminates the `Event` block.|  
  
## Remarks  
 Once the event has been declared, use the `RaiseEvent` statement to raise the event. A typical event might be declared and raised as shown in the following fragments:  
  
 [!CODE [VbVbalrEvents#13](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#13)]  
  
> [!NOTE]
>  You can declare event arguments just as you do arguments of procedures, with the following exceptions: events cannot have named arguments, `ParamArray` arguments, or `Optional` arguments. Events do not have return values.  
  
 To handle an event, you must associate it with an event handler subroutine using either the `Handles` or `AddHandler` statement. The signatures of the subroutine and the event must match. To handle a shared event, you must use the `AddHandler` statement.  
  
 You can use `Event` only at module level. This means the *declaration context* for an event must be a class, structure, module, or interface, and cannot be a source file, namespace, procedure, or block. For more information, see [Declaration Contexts and Default Access Levels](../vs140/Declaration-Contexts-and-Default-Access-Levels--Visual-Basic-.md).  
  
 In most circumstances, you can use the first syntax in the Syntax section of this topic for declaring events. However, some scenarios require that you have more control over the detailed behavior of the event. The last syntax in the Syntax section of this topic, which uses the `Custom` keyword, provides that control by enabling you to define custom events. In a custom event, you specify exactly what occurs when code adds or removes an event handler to or from the event, or when code raises the event. For examples, see [How to: Declare Events That Conserve Memory Use](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md) and [How to: Declare Events That Avoid Blocking](../vs140/How-to--Declare-Custom-Events-To-Avoid-Blocking--Visual-Basic-.md).  
  
## Example  
 The following example uses events to count down seconds from 10 to 0. The code illustrates several of the event-related methods, properties, and statements. This includes the `RaiseEvent` statement.  
  
 The class that raises an event is the event source, and the methods that process the event are the event handlers. An event source can have multiple handlers for the events it generates. When the class raises the event, that event is raised on every class that has elected to handle events for that instance of the object.  
  
 The example also uses a form (`Form1`) with a button (`Button1`) and a text box (`TextBox1`). When you click the button, the first text box displays a countdown from 10 to 0 seconds. When the full time (10 seconds) has elapsed, the first text box displays "Done".  
  
 The code for `Form1` specifies the initial and terminal states of the form. It also contains the code executed when events are raised.  
  
 To use this example, open a new Windows Forms project. Then add a button named `Button1` and a text box named `TextBox1` to the main form, named `Form1`. Then right-click the form and click **View Code** to open the code editor.  
  
 Add a `WithEvents` variable to the declarations section of the `Form1` class:  
  
 [!CODE [VbVbalrEvents#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#14)]  
  
 Add the following code to the code for `Form1`. Replace any duplicate procedures that may exist, such as `Form_Load` or `Button_Click`.  
  
 [!CODE [VbVbalrEvents#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#15)]  
  
 Press F5 to run the previous example, and click the button labeled **Start**. The first text box starts to count down the seconds. When the full time (10 seconds) has elapsed, the first text box displays "Done".  
  
> [!NOTE]
>  The `My.Application.DoEvents` method does not process events in the same way the form does. To enable the form to handle the events directly, you can use multithreading. For more information, see [Threading (C# and Visual Basic)](../vs140/Threading--C#-and-Visual-Basic-.md).  
  
## See Also  
 [RaiseEvent Statement](../vs140/RaiseEvent-Statement.md)   
 [Implements Statement](../vs140/Implements-Statement.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)   
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [RemoveHandler Statement](../vs140/RemoveHandler-Statement.md)   
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [How to: Declare Events That Conserve Memory Use](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md)   
 [How to: Declare Events That Avoid Blocking](../vs140/How-to--Declare-Custom-Events-To-Avoid-Blocking--Visual-Basic-.md)   
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)   
 [Shadows](../vs140/Shadows--Visual-Basic-.md)