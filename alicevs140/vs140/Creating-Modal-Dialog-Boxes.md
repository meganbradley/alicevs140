---
title: "Creating Modal Dialog Boxes"
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
ms.assetid: 26c7a68c-79f6-4862-a5a8-6024984644d2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating Modal Dialog Boxes
To create a modal dialog box, call either of the two public constructors declared in [CDialog](../vs140/CDialog-Class.md). Next, call the dialog object's [DoModal](../vs140/CDialog--DoModal.md) member function to display the dialog box and manage interaction with it until the user chooses OK or Cancel. This management by `DoModal` is what makes the dialog box modal. For modal dialog boxes, `DoModal` loads the dialog resource.  
  
## See Also  
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)