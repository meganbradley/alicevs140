---
title: "Working with Dynamic Objects (Visual Basic)"
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
ms.assetid: bdee2a00-07ff-46f9-86dd-fdac9b99cc97
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Working with Dynamic Objects (Visual Basic)
Dynamic objects provide another way, other than the `Object` type, to late bind to an object at run time. A dynamic object exposes members such as properties and methods at run time by using dynamic interfaces that are defined in the <xref:System.Dynamic?qualifyHint=False> namespace. You can use the classes in the <xref:System.Dynamic?qualifyHint=False> namespace to create objects that work with data structures that do not match a static type or format. You can also use the dynamic objects that are defined in dynamic languages such as IronPython and IronRuby. For examples that show how to create dynamic objects or use a dynamic object defined in a dynamic language, see [Walkthrough: Creating and Using Dynamic Objects (C# and Visual Basic)](../Topic/Walkthrough:%20Creating%20and%20Using%20Dynamic%20Objects%20\(C%23%20and%20Visual%20Basic\).md), <xref:System.Dynamic.DynamicObject?qualifyHint=False>, or <xref:System.Dynamic.ExpandoObject?qualifyHint=False>.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] binds to objects from the dynamic language runtime and dynamic languages such as IronPython and IronRuby by using the <xref:System.Dynamic.IDynamicMetaObjectProvider?qualifyHint=False> interface. Examples of classes that implement the `IDynamicMetaObjectProvider` interface are the <xref:System.Dynamic.DynamicObject?qualifyHint=False> and <xref:System.Dynamic.ExpandoObject?qualifyHint=False> classes.  
  
 If a late-bound call is made to an object that implements the `IDynamicMetaObjectProvider` interface, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] binds to the dynamic object by using that interface. If a late-bound call is made to an object that does not implement the `IDynamicMetaObjectProvider` interface, or if the call to the `IDynamicMetaObjectProvider` interface fails, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] binds to the object by using the late-binding capabilities of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] runtime.  
  
## See Also  
 <xref:System.Dynamic.DynamicObject?qualifyHint=False>   
 <xref:System.Dynamic.ExpandoObject?qualifyHint=False>   
 [Walkthrough: Creating and Using Dynamic Objects (C# and Visual Basic)](../Topic/Walkthrough:%20Creating%20and%20Using%20Dynamic%20Objects%20\(C%23%20and%20Visual%20Basic\).md)   
 [Early and Late Binding](../vs140/Early-and-Late-Binding--Visual-Basic-.md)