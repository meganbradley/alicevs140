---
title: "Modal and Modeless Dialog Boxes"
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
ms.assetid: e83df336-5994-4b8f-8233-7942f997315b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Modal and Modeless Dialog Boxes
You can use class [CDialog](../vs140/CDialog-Class.md) to manage two kinds of dialog boxes:  
  
-   *Modal dialog boxes*, which require the user to respond before continuing the program  
  
-   *Modeless dialog boxes*, which stay on the screen and are available for use at any time but permit other user activities  
  
 The resource editing and procedures for creating a dialog template are the same for modal and modeless dialog boxes.  
  
 Creating a dialog box for your program requires the following steps:  
  
1.  Use the [dialog editor](../vs140/Dialog-Editor.md) to design the dialog box and create its dialog-template resource.  
  
2.  Create a dialog class.  
  
3.  Connect the [dialog resource's controls to message handlers](../vs140/Adding-Event-Handlers-for-Dialog-Box-Controls.md) in the dialog class.  
  
4.  Add data members associated with the dialog box's controls and to specify [dialog data exchange](../vs140/Dialog-Data-Exchange.md) and [dialog data validations](../vs140/Dialog-Data-Validation.md) for the controls.  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)   
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)