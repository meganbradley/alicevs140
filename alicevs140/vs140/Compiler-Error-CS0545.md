---
title: "Compiler Error CS0545"
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
ms.topic: error-reference
ms.assetid: f8c50376-76c4-46ac-9ee1-76cc58005cea
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0545
'function' : cannot override because 'property' does not have an overridable get accessor  
  
 A try was made to define an override for a property accessor when the base class has no such definition to override. You can resolve this error by:  
  
-   Adding a `set` accessor in the base class.  
  
-   Removing the `set` accessor from the derived class.  
  
-   Hiding the base class property by adding the [new](../vs140/new--C#-Reference-.md) keyword to a property in a derived class.  
  
-   Making the base class property [virtual](../vs140/virtual--C#-Reference-.md).  
  
 For more information, see [Using Properties (C# Programming Guide)](../vs140/Using-Properties--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0545.  
  
```  
// CS0545.cs  
// compile with: /target:library  
// CS0545  
public class a  
{  
   public virtual int i  
   {  
      set {}  
  
      // Uncomment the following line to resolve.  
      // get { return 0; }  
   }  
}  
  
public class b : a  
{  
   public override int i  
   {  
      get { return 0; }  
      set {}   // OK  
   }  
}  
```