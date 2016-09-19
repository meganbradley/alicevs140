---
title: "How to: Raise Base Class Events in Derived Classes (C# Programming Guide)"
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
ms.assetid: 2d20556a-0aad-46fc-845e-f85d86ea617a
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Raise Base Class Events in Derived Classes (C# Programming Guide)
The following simple example shows the standard way to declare events in a base class so that they can also be raised from derived classes. This pattern is used extensively in Windows Forms classes in the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] class library.  
  
 When you create a class that can be used as a base class for other classes, you should consider the fact that events are a special type of delegate that can only be invoked from within the class that declared them. Derived classes cannot directly invoke events that are declared within the base class. Although sometimes you may want an event that can only be raised by the base class, most of the time, you should enable the derived class to invoke base class events. To do this, you can create a protected invoking method in the base class that wraps the event. By calling or overriding this invoking method, derived classes can invoke the event indirectly.  
  
> [!NOTE]
>  Do not declare virtual events in a base class and override them in a derived class. The C# compiler does not handle these correctly and it is unpredictable whether a subscriber to the derived event will actually be subscribing to the base class event.  
  
## Example  
 [!CODE [csProgGuideEvents#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEvents#1)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Events (C# Programmer's Reference)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)   
 [Delegates (C# Programmer's Reference)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [Creating Event Handlers in Windows Forms](assetId:///6514e530-c6b8-489c-a8d2-eda7b7072701)