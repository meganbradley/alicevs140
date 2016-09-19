---
title: "Type-Safe Access to Controls in a Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 67021025-dd93-4d6a-8bed-a1348fe50685
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type-Safe Access to Controls in a Dialog Box
The controls in a dialog box can use the interfaces of MFC control classes such as `CListBox` and `CEdit`. You can create a control object and attach it to a dialog control. Then you can access the control through its class interface, calling member functions to operate on the control. The methods described here are designed to give you type-safe access to a control. This is especially useful for controls such as edit boxes and list boxes.  
  
 There are two approaches to making a connection between a control in a dialog box and a C++ control member variable in a `CDialog`-derived class:  
  
-   [Without Code Wizards](../vs140/Type-Safe-Access-to-Controls-Without-Code-Wizards.md)  
  
-   [With Code Wizards](../vs140/Type-Safe-Access-to-Controls-With-Code-Wizards.md)  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)