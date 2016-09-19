---
title: "&#39;&lt;elementname&gt;&#39; for the Imports alias to &#39;&lt;qualifiedelementname&gt;&#39; does not refer to a Namespace, Class, Structure, Interface, Enum or Module"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfa66627-516a-4955-977d-92372bcea090
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;elementname&gt;&#39; for the Imports alias to &#39;&lt;qualifiedelementname&gt;&#39; does not refer to a Namespace, Class, Structure, Interface, Enum or Module
An [Imports Statement](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) specifies a programming element that cannot be imported.  
  
 The `Imports` statement is used to reduce or remove the need for a qualifying string in front of an element name. You qualify the element in the `Imports` statement itself to provide an unambiguous path to a unique declaration of the element. Thereafter, you do not need to qualify references to the element.  
  
 `Imports` is most commonly used for namespaces, but you can also import a class, module, structure, interface, or enumeration to allow reference to its elements without a long qualifying string.  
  
 For more information, see "Importing Containing Elements" in [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](assetId:///9601e39f-1911-44e1-ace5-3f6e090408b9).  
  
 **Error ID:** BC30798  
  
### To correct this error  
  
1.  Check the spelling of the elements in the qualification string in the `Imports` statement, especially the last element in the string, which is the element you are qualifying.  
  
2.  Verify that the element you are qualifying is of an eligible type (namespace, class, module, structure, interface, or enumeration). If it is not, remove the `Imports` statement.  
  
## See Also  
 [References and the Imports Statement](../vs140/References-and-the-Imports-Statement--Visual-Basic-.md)