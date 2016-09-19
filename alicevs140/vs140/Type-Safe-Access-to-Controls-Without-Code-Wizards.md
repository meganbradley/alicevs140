---
title: "Type-Safe Access to Controls Without Code Wizards"
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
ms.assetid: 325b4927-d49b-42b4-8e0b-fc84f31fb059
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type-Safe Access to Controls Without Code Wizards
The first approach to creating type-safe access to controls uses an inline member function to cast the return type of class `CWnd`'s `GetDlgItem` member function to the appropriate C++ control type, as in this example:  
  
 [!CODE [NVC_MFCControlLadenDialog#50](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#50)]  
  
 You can then use this member function to access the control in a type-safe manner with code similar to the following:  
  
 [!CODE [NVC_MFCControlLadenDialog#51](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#51)]  
  
## See Also  
 [Type-Safe Access to Controls in a Dialog Box](../vs140/Type-Safe-Access-to-Controls-in-a-Dialog-Box.md)   
 [Type-Safe Access to Controls With Code Wizards](../vs140/Type-Safe-Access-to-Controls-With-Code-Wizards.md)