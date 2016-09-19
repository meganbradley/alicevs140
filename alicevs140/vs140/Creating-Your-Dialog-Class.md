---
title: "Creating Your Dialog Class"
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
ms.assetid: d5321741-da41-47a8-bb1c-6a0e8b28c4c1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating Your Dialog Class
For each dialog box in your program, create a new dialog class to work with the dialog resource.  
  
 [Adding a Class](../vs140/Adding-a-Class--Visual-C---.md) explains how to create a new dialog class. When you create a dialog class with the Add Class Wizard, it writes the following items in the .H and .CPP files you specify:  
  
 In the .H file:  
  
-   A class declaration for the dialog class. The class is derived from [CDialog](../vs140/CDialog-Class.md).  
  
 In the .CPP file:  
  
-   A message map for the class.  
  
-   A standard constructor for the dialog box.  
  
-   An override of the [DoDataExchange](../vs140/CWnd--DoDataExchange.md) member function. Edit this function. It is used for dialog data exchange and validation capabilities as described later in [Dialog data exchange and validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## See Also  
 [Creating a Dialog Class with Code Wizards](../vs140/Creating-a-Dialog-Class-with-Code-Wizards.md)   
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)