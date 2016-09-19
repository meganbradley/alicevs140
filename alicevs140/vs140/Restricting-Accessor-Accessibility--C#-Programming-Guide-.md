---
title: "Restricting Accessor Accessibility (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e655798-e112-4301-a680-6310a6e012e1
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Restricting Accessor Accessibility (C# Programming Guide)
The [get](../vs140/get--C#-Reference-.md) and [set](../vs140/set--C#-Reference-.md) portions of a property or indexer are called *accessors*. By default these accessors have the same visibility, or access level: that of the property or indexer to which they belong. For more information, see [accessibility levels](../vs140/Accessibility-Levels--C#-Reference-.md). However, it is sometimes useful to restrict access to one of these accessors. Typically, this involves restricting the accessibility of the `set` accessor, while keeping the `get` accessor publicly accessible. For example:  
  
 [!CODE [csProgGuideIndexers#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#6)]  
  
 In this example, a property called `Name` defines a `get` and `set` accessor. The `get` accessor receives the accessibility level of the property itself, `public` in this case, while the `set` accessor is explicitly restricted by applying the [protected](../vs140/protected--C#-Reference-.md) access modifier to the accessor itself.  
  
## Restrictions on Access Modifiers on Accessors  
 Using the accessor modifiers on properties or indexers is subject to these conditions:  
  
-   You cannot use accessor modifiers on an interface or an explicit [interface](../vs140/interface--C#-Reference-.md) member implementation.  
  
-   You can use accessor modifiers only if the property or indexer has both `set` and `get` accessors. In this case, the modifier is permitted on one only of the two accessors.  
  
-   If the property or indexer has an [override](../vs140/override--C#-Reference-.md) modifier, the accessor modifier must match the accessor of the overridden accessor, if any.  
  
-   The accessibility level on the accessor must be more restrictive than the accessibility level on the property or indexer itself.  
  
## Access Modifiers on Overriding Accessors  
 When you override a property or indexer, the overridden accessors must be accessible to the overriding code. Also, the accessibility level of both the property/indexer, and that of the accessors must match the corresponding overridden property/indexer and the accessors. For example:  
  
 [!CODE [csProgGuideIndexers#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#7)]  
  
## Implementing Interfaces  
 When you use an accessor to implement an interface, the accessor may not have an access modifier. However, if you implement the interface using one accessor, such as `get`, the other accessor can have an access modifier, as in the following example:  
  
 [!CODE [csProgGuideIndexers#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#8)]  
  
## Accessor Accessibility Domain  
 If you use an access modifier on the accessor, the [accessibility domain](../vs140/Accessibility-Domain--C#-Reference-.md) of the accessor is determined by this modifier.  
  
 If you did not use an access modifier on the accessor, the accessibility domain of the accessor is determined by the accessibility level of the property or indexer.  
  
## Example  
 The following example contains three classes, `BaseClass`, `DerivedClass`, and `MainClass`. There are two properties on the `BaseClass`, `Name` and `Id` on both classes. The example demonstrates how the property `Id` on `DerivedClass` can be hidden by the property `Id` on `BaseClass` when you use a restrictive access modifier such as [protected](../vs140/protected--C#-Reference-.md) or [private](../vs140/private--C#-Reference-.md). Therefore, when you assign values to this property, the property on the `BaseClass` class is called instead. Replacing the access modifier by [public](../vs140/public--C#-Reference-.md) will make the property accessible.  
  
 The example also demonstrates that a restrictive access modifier, such as `private` or `protected`, on the `set` accessor of the `Name` property in `DerivedClass` prevents access to the accessor and generates an error when you assign to it.  
  
 [!CODE [csProgGuideIndexers#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#5)]  
  
## Comments  
 Notice that if you replace the declaration `new private string Id` by `new public string Id`, you get the output:  
  
 `Name and ID in the base class: Name-BaseClass, ID-BaseClass`  
  
 `Name and ID in the derived class: John, John123`  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md)   
 [Indexers (C# Programming Guide)](../vs140/Indexers--C#-Programming-Guide-.md)   
 [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)