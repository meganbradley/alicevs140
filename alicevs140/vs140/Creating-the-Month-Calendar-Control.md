---
title: "Creating the Month Calendar Control"
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
ms.assetid: 185cc642-85e9-4365-8a4c-d90b75b010f7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating the Month Calendar Control
How the month calendar control is created depends on whether you are using the control in a dialog box or creating it in a nondialog window.  
  
### To use CMonthCalCtrl directly in a dialog box  
  
1.  In the dialog editor, add a Month Calendar Control to your dialog template resource. Specify its control ID.  
  
2.  Specify any styles required, using the Properties dialog box of the month calendar control.  
  
3.  Use the [Add Member Variable Wizard](../vs140/Adding-a-Member-Variable---Visual-C---.md) to add a member variable of type [CMonthCalCtrl](../vs140/CMonthCalCtrl-Class.md) with the Control property. You can use this member to call `CMonthCalCtrl` member functions.  
  
4.  Use the Properties window to map handler functions in the dialog class for any month calendar control notification messages you need to handle (see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md)).  
  
5.  In [OnInitDialog](../vs140/CDialog--OnInitDialog.md), set any additional styles for the `CMonthCalCtrl` object.  
  
### To use CMonthCalCtrl in a nondialog window  
  
1.  Define the control in the view or window class.  
  
2.  Call the control's [Create](../vs140/CMonthCalCtrl--Create.md) member function, possibly in [OnInitialUpdate](../vs140/CView--OnInitialUpdate.md), possibly as early as the parent window's [OnCreate](../vs140/CWnd--OnCreate.md) handler function (if you're subclassing the control). Set the styles for the control.  
  
## See Also  
 [Using CMonthCalCtrl](../vs140/Using-CMonthCalCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)