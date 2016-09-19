---
title: "Defining Mnemonics (Access Keys)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 60a85435-aa30-4c5c-98b6-42fb045b9eb2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Defining Mnemonics (Access Keys)
Normally, keyboard users move the input focus from one control to another in a dialog box with the TAB and ARROW keys. However, you can define an access key (a mnemonic or easy-to-remember name) that allows users to choose a control by pressing a single key.  
  
### To define an access key for a control with a visible caption (push buttons, check boxes, and radio buttons)  
  
1.  Select the control on the dialog box.  
  
2.  In the [Properties Window](../vs140/Properties-Window.md), in the **Caption** property, type a new name for the control, typing an ampersand (**&**) in front of the letter you want as the access key for that control. For example, `&Radio1`.  
  
3.  Press **Enter**.  
  
     An underline appears in the displayed caption to indicate the access key, for example, **R**adio1.  
  
### To define an access key for a control without a visible caption  
  
1.  Make a caption for the control by using a **Static Text** control in the [Toolbox](../vs140/Toolbox.md).  
  
2.  In the static text caption, type an ampersand (**&**) in front of the letter you want as the access key.  
  
3.  Make sure the static text control immediately precedes the control it labels in the tab order.  
  
 All the access keys within a dialog box should be unique.  
  
#### To check for duplicate access keys  
  
1.  On the **Format** menu, click **Check Mnemonics**.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
### Requirements  
 Win32  
  
## See Also  
 [Controls in Dialog Boxes](../vs140/Controls-in-Dialog-Boxes.md)   
 [Controls](../vs140/Controls--MFC-.md)