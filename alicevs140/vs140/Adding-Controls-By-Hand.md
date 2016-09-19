---
title: "Adding Controls By Hand"
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
ms.assetid: bc843e59-0c51-4b5b-8bf2-343f716469d2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding Controls By Hand
You can either [add controls to a dialog box with the dialog editor](../vs140/Using-the-Dialog-Editor-to-Add-Controls.md) or add them yourself, with code.  
  
 To create a control object yourself, you will usually embed the C++ control object in a C++ dialog or frame-window object. Like many other objects in the framework, controls require two-stage construction. You should call the control's **Create** member function as part of creating the parent dialog box or frame window. For dialog boxes, this is usually done in [OnInitDialog](../vs140/CDialog--OnInitDialog.md), and for frame windows, in [OnCreate](../vs140/CWnd--OnCreate.md).  
  
 The following example shows how you might declare a `CEdit` object in the class declaration of a derived dialog class and then call the **Create** member function in `OnInitDialog`. Because the `CEdit` object is declared as an embedded object, it is automatically constructed when the dialog object is constructed, but it must still be initialized with its own **Create** member function.  
  
 [!CODE [NVC_MFCControlLadenDialog#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#1)]  
  
 The following `OnInitDialog` function sets up a rectangle, then calls **Create** to create the Windows edit control and attach it to the uninitialized `CEdit` object.  
  
 [!CODE [NVC_MFCControlLadenDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#2)]  
  
 After creating the edit object, you can also set the input focus to the control by calling the `SetFocus` member function. Finally, you return 0 from `OnInitDialog` to show that you set the focus. If you return a nonzero value, the dialog manager sets the focus to the first control item in the dialog item list. In most cases, you'll want to add controls to your dialog boxes with the dialog editor.  
  
## See Also  
 [Making and Using Controls](../vs140/Making-and-Using-Controls.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)   
 [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md)