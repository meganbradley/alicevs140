---
title: "Creating and Displaying Dialog Boxes"
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
ms.assetid: 1c5219ee-8b46-44bc-9708-83705d4f248b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating and Displaying Dialog Boxes
Creating a dialog object is a two-phase operation. First, construct the dialog object, then create the dialog window. Modal and modeless dialog boxes differ somewhat in the process used to create and display them. The following table lists how modal and modeless dialog boxes are normally constructed and displayed.  
  
### Dialog Creation  
  
|Dialog type|How to create it|  
|-----------------|----------------------|  
|[Modeless](../vs140/Creating-Modeless-Dialog-Boxes.md)|Construct `CDialog`, then call **Create** member function.|  
|[Modal](../vs140/Creating-Modal-Dialog-Boxes.md)|Construct `CDialog`, then call `DoModal` member function.|  
  
 You can, if you want, create your dialog box from an [in-memory dialog template](../vs140/Using-a-Dialog-Template-in-Memory.md) that you have constructed rather than from a dialog template resource. This is an advanced topic, however.  
  
## See Also  
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)