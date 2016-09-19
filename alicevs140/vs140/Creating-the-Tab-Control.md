---
title: "Creating the Tab Control"
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
ms.assetid: 3a9c2d64-f5f4-41ea-84ab-fceb73c3dbdc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating the Tab Control
How the tab control is created depends on whether you are using the control in a dialog box or creating it in a nondialog window.  
  
### To use CTabCtrl directly in a dialog box  
  
1.  In the dialog editor, add a Tab Control to your dialog template resource. Specify its control ID.  
  
2.  Use the [Add Member Variable Wizard](../vs140/Adding-a-Member-Variable---Visual-C---.md) to add a member variable of type [CTabCtrl](../vs140/CTabCtrl-Class.md) with the Control property. You can use this member to call `CTabCtrl` member functions.  
  
3.  Map handler functions in the dialog class for any tab control notification messages you need to handle. For more information, see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md).  
  
4.  In [OnInitDialog](../vs140/CDialog--OnInitDialog.md), set the styles for the `CTabCtrl`.  
  
### To use CTabCtrl in a nondialog window  
  
1.  Define the control in the view or window class.  
  
2.  Call the control's [Create](../vs140/CTabCtrl--Create.md) member function, possibly in [OnInitialUpdate](../vs140/CView--OnInitialUpdate.md), possibly as early as the parent window's [OnCreate](../vs140/CWnd--OnCreate.md) handler function (if you're subclassing the control). Set the styles for the control.  
  
 After the `CTabCtrl` object has been created, you can set or clear the following extended styles:  
  
-   **TCS_EX_FLATSEPARATORS** The tab control will draw separators between the tab items. This extended style only affects tab controls that have the **TCS_BUTTONS** and **TCS_FLATBUTTONS** styles. By default, creating the tab control with the **TCS_FLATBUTTONS** style sets this extended style.  
  
-   **TCS_EX_REGISTERDROP** The tab control generates **TCN_GETOBJECT** notification messages to request a drop target object when an object is dragged over the tab items in the control.  
  
    > [!NOTE]
    >  To receive the **TCN_GETOBJECT** notification, you must initialize the OLE libraries with a call to [AfxOleInit](../vs140/AfxOleInit.md).  
  
 These styles can be retrieved and set, after the control has been created, with respective calls to the [GetExtendedStyle](../vs140/CTabCtrl--GetExtendedStyle.md) and [SetExtendedStyle](../vs140/CTabCtrl--SetExtendedStyle.md) member functions.  
  
 For instance, set the **TCS_EX_FLATSEPARATORS** style with the following lines of code:  
  
 [!CODE [NVC_MFCControlLadenDialog#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#33)]  
  
 Clear the **TCS_EX_FLATSEPARATORS** style from a `CTabCtrl` object with the following lines of code:  
  
 [!CODE [NVC_MFCControlLadenDialog#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#34)]  
  
 This will remove the separators that appear between the buttons of your `CTabCtrl` object.  
  
## See Also  
 [Using CTabCtrl](../vs140/Using-CTabCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)