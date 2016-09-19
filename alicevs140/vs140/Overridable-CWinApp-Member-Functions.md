---
title: "Overridable CWinApp Member Functions"
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
ms.assetid: 07183d5e-734b-45d9-a8b6-9dde4adac0b4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overridable CWinApp Member Functions
[CWinApp](../vs140/CWinApp-Class.md) provides several key overridable member functions (`CWinApp` overrides these members from class [CWinThread](../vs140/CWinThread-Class.md), from which `CWinApp` derives):  
  
-   [InitInstance](../vs140/InitInstance-Member-Function.md)  
  
-   [Run](../vs140/Run-Member-Function.md)  
  
-   [ExitInstance](../vs140/ExitInstance-Member-Function.md)  
  
-   [OnIdle](../vs140/OnIdle-Member-Function.md)  
  
 The only `CWinApp` member function that you must override is `InitInstance`.  
  
## See Also  
 [CWinApp: The Application Class](../vs140/CWinApp--The-Application-Class.md)