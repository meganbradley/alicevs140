---
title: "GetType Operator (Visual Basic)"
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
ms.assetid: 4f733297-2503-4607-850c-15eba65fff90
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetType Operator (Visual Basic)
Returns a <xref:System.Type?qualifyHint=False> object for the specified type. The <xref:System.Type?qualifyHint=False> object provides information about the type such as its properties, methods, and events.  
  
## Syntax  
  
```  
GetType(typename)  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`typename`|The name of the type for which you desire information.|  
  
## Remarks  
 The `GetType` operator returns the <xref:System.Type?qualifyHint=False> object for the specified `typename`. You can pass the name of any defined type in `typename`. This includes the following:  
  
-   Any Visual Basic data type, such as `Boolean` or `Date`.  
  
-   Any .NET Framework class, structure, module, or interface, such as <xref:System.ArgumentException?qualifyHint=True> or <xref:System.Double?qualifyHint=True>.  
  
-   Any class, structure, module, or interface defined by your application.  
  
-   Any array defined by your application.  
  
-   Any delegate defined by your application.  
  
-   Any enumeration defined by Visual Basic, the .NET Framework, or your application.  
  
 If you want to get the type object of an object variable, use the <xref:System.Type.GetType?qualifyHint=True> method.  
  
 The `GetType` operator can be useful in the following circumstances:  
  
-   You must access the metadata for a type at run time. The <xref:System.Type?qualifyHint=False> object supplies metadata such as type members and deployment information. You need this, for example, to reflect over an assembly. For more information, see <xref:System.Reflection?qualifyHint=True>.  
  
-   You want to compare two object references to see if they refer to instances of the same type. If they do, `GetType` returns references to the same <xref:System.Type?qualifyHint=False> object.  
  
## Example  
 The following examples show the `GetType` operator in use.  
  
 [!CODE [VbVbalrOperators#26](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#26)]  
  
## See Also  
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Operators and Expressions](../vs140/Operators-and-Expressions-in-Visual-Basic.md)