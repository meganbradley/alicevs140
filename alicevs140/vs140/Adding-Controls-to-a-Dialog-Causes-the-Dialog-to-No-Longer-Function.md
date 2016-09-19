---
title: "Adding Controls to a Dialog Causes the Dialog to No Longer Function"
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
ms.assetid: b2dd4574-ea59-4343-8d65-b387cead5da6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding Controls to a Dialog Causes the Dialog to No Longer Function
After adding a common control or rich edit control to a dialog box, it will not appear when you test the dialog box or the dialog itself will not appear.  
  
 **Example of the problem**  
  
1.  Create a Win32 project, modifying the application settings so you create a Windows application (not a console app).  
  
2.  In [Resource View](../vs140/Resource-View-Window.md), double click on the .rc file.  
  
3.  Under the dialog option, double click the **About** box.  
  
4.  Add an **IP Address Control** to the dialog box.  
  
5.  Save and **Rebuild all**.  
  
6.  Execute the program.  
  
7.  On the dialog box's **Help** menu, click the **About** command; no dialog box is displayed.  
  
 **The cause**  
  
 Currently, the Dialog editor does not automatically add code to your project when you drag and drop the following common controls or rich edit controls onto a dialog box. Nor does Visual Studio provide an error or warning when this problem occurs. You must add the code for the control manually.  
  
||||  
|-|-|-|  
|Slider Control|Tree Control|Date Time Picker|  
|Spin Control|Tab Control|Month Calendar|  
|Progress Control|Animation Control|IP Address Control|  
|Hot Key|Rich Edit Control|Extended Combo Box|  
|List Control|Rich Edit 2.0 Control|Custom Control|  
  
## The fix for common controls  
 In order to use common controls on a dialog box, you need to call [InitCommonControlsEx](http://msdn.microsoft.com/library/windows/desktop/bb775697) or **AFXInitCommonControls** before you create the dialog box.  
  
## The fix for RichEdit controls  
 You must call **LoadLibrary** for rich edit controls. For more information, see [Using the RichEdit 1.0 Control with MFC](../vs140/Using-the-RichEdit-1.0-Control-with-MFC.md), [About Rich Edit Controls](http://msdn.microsoft.com/library/windows/desktop/bb787873) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)], and [Overview of the Rich Edit Control](../vs140/Overview-of-the-Rich-Edit-Control.md).  
  
## Requirements  
 Win32  
  
## See Also  
 [Troubleshooting the Dialog Editor](../vs140/Troubleshooting-the-Dialog-Editor.md)   
 [Dialog Editor](../vs140/Dialog-Editor.md)