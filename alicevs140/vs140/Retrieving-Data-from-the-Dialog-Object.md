---
title: "Retrieving Data from the Dialog Object"
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
ms.assetid: bdca2b61-6b53-4c2e-b426-8712c7a38ec0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Retrieving Data from the Dialog Object
The framework provides an easy way to initialize the values of controls in a dialog box and to retrieve values from the controls. The more laborious manual approach is to call functions such as the `SetDlgItemText` and `GetDlgItemText` member functions of class `CWnd`, which apply to control windows. With these functions, you access each control individually to set or get its value, calling functions such as `SetWindowText` and `GetWindowText`. The framework's approach automates both initialization and retrieval.  
  
 Dialog data exchange (DDX) lets you exchange data between the controls in the dialog box and member variables in the dialog object more easily. This exchange works both ways. To initialize the controls in the dialog box, you can set the values of data members in the dialog object, and the framework will transfer the values to the controls before the dialog box is displayed. Then you can at any time update the dialog data members with data entered by the user. At that point, you can use the data by referring to the data member variables.  
  
 You can also arrange for the values of dialog controls to be validated automatically with dialog data validation (DDV).  
  
 DDX and DDV are explained in more detail in [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
 For a modal dialog box, you can retrieve any data the user entered when `DoModal` returns **IDOK** but before the dialog object is destroyed. For a modeless dialog box, you can retrieve data from the dialog object at any time by calling `UpdateData` with the argument **TRUE** and then accessing dialog class member variables. This subject is discussed in more detail in [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## See Also  
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)