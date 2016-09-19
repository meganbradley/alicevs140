---
title: "Spin Button Member Functions"
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
ms.assetid: a08a26fd-b803-4cbe-a509-395fa357d057
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Spin Button Member Functions
There are several member functions available for the spin control ([CSpinButtonCtrl](../vs140/CSpinButtonCtrl-Class.md)). Use these functions to change the following attributes of the spin button.  
  
-   **Acceleration** You can adjust the rate at which the position changes when the user holds down the arrow button. To work with acceleration, use the [SetAccel](../vs140/CSpinButtonCtrl--SetAccel.md) and [GetAccel](../vs140/CSpinButtonCtrl--GetAccel.md) member functions.  
  
-   **Base** You can change the base (either 10 or 16) used to display the position in the caption of the buddy window. To work with the base, use the [GetBase](../vs140/CSpinButtonCtrl--GetBase.md) and [SetBase](../vs140/CSpinButtonCtrl--SetBase.md) member functions.  
  
-   **Buddy Window** You can dynamically set the buddy window. To query or change which control is the buddy window, use the [GetBuddy](../vs140/CSpinButtonCtrl--GetBuddy.md) and [SetBuddy](../vs140/CSpinButtonCtrl--SetBuddy.md) member functions.  
  
-   **Position** You can query and change the position. To work directly with position, use the [GetPos](../vs140/CSpinButtonCtrl--GetPos.md) and [SetPos](../vs140/CSpinButtonCtrl--SetPos.md) member functions. Since the caption of the buddy control may have changed (for example, in the case that the buddy is an edit control), `GetPos` retrieves the current caption and adjusts the position accordingly.  
  
-   **Range** You can change the maximum and minimum positions for the spin button. By default, the maximum is set to 0, and the minimum is set to 100. Since the default maximum is less than the default minimum, the actions of the arrow buttons is counter-intuitive. Typically, you will set the range using the [SetRange](../vs140/CSpinButtonCtrl--SetRange.md) member function. To query the range use [GetRange](../vs140/CSpinButtonCtrl--GetRange.md).  
  
## See Also  
 [Using CSpinButtonCtrl](../vs140/Using-CSpinButtonCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)