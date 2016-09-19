---
title: "Accessibility Levels (C# Reference)"
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
ms.assetid: dc083921-0073-413e-8936-a613e8bb7df4
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accessibility Levels (C# Reference)
Use the access modifiers, [public](../vs140/public--C#-Reference-.md), [protected](../vs140/protected--C#-Reference-.md), [internal](../vs140/internal--C#-Reference-.md), or [private](../vs140/private--C#-Reference-.md), to specify one of the following declared accessibility levels for members.  
  
|Declared accessibility|Meaning|  
|----------------------------|-------------|  
|`public`|Access is not restricted.|  
|`protected`|Access is limited to the containing class or types derived from the containing class.|  
|`internal`|Access is limited to the current assembly.|  
|`protected` `internal`|Access is limited to the current assembly or types derived from the containing class.|  
|`private`|Access is limited to the containing type.|  
  
 Only one access modifier is allowed for a member or type, except when you use the `protected` `internal` combination.  
  
 Access modifiers are not allowed on namespaces. Namespaces have no access restrictions.  
  
 Depending on the context in which a member declaration occurs, only certain declared accessibilities are permitted. If no access modifier is specified in a member declaration, a default accessibility is used.  
  
 Top-level types, which are not nested in other types, can only have `internal` or `public` accessibility. The default accessibility for these types is `internal`.  
  
 Nested types, which are members of other types, can have declared accessibilities as indicated in the following table.  
  
|Members of|Default member accessibility|Allowed declared accessibility of the member|  
|----------------|----------------------------------|--------------------------------------------------|  
|`enum`|`public`|None|  
|`class`|`private`|`public`<br /><br /> `protected`<br /><br /> `internal`<br /><br /> `private`<br /><br /> `protected` `internal`|  
|`interface`|`public`|None|  
|`struct`|`private`|`public`<br /><br /> `internal`<br /><br /> `private`|  
  
 The accessibility of a nested type depends on its [accessibility domain](../vs140/Accessibility-Domain--C#-Reference-.md), which is determined by both the declared accessibility of the member and the accessibility domain of the immediately containing type. However, the accessibility domain of a nested type cannot exceed that of the containing type.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md)   
 [Accessibility Domain](../vs140/Accessibility-Domain--C#-Reference-.md)   
 [Restrictions on Using Accessibility Levels](../vs140/Restrictions-on-Using-Accessibility-Levels--C#-Reference-.md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [public (C# Programmer's Reference)](../vs140/public--C#-Reference-.md)   
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Programmer's Reference)](../vs140/internal--C#-Reference-.md)