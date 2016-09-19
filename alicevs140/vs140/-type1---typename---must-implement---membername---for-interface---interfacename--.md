---
title: "&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;membername&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;"
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
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;membername&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;
'<typename\>' must implement '<membername\>' for interface '<interfacename\>'. Implementing property must have matching 'ReadOnly'/'WriteOnly' specifiers.  
  
 A class or structure claims to implement an interface but does not implement a procedure, property, or event defined by the interface. Every member of the interface must be implemented.  
  
 **Error ID:** BC30154  
  
### To correct this error  
  
1.  Declare a member with the same name and signature as defined in the interface. Be sure to include at least the `End Function`, `End Sub`, or `End Property` statement.  
  
2.  Add an `Implements` clause to the end of the `Function`, `Sub`, `Property`, or `Event` statement. For example:  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3.  When implementing a property, make sure that `ReadOnly` or `WriteOnly` is used in the same way as in the interface definition.  
  
4.  When implementing a property, declare `Get` and `Set` procedures, as appropriate.  
  
## See Also  
 [Implements Statement](../vs140/Implements-Statement.md)   
 [Interfaces (Visual Basic)](../vs140/Interfaces--Visual-Basic-.md)