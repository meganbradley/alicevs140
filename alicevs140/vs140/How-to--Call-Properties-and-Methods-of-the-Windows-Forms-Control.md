---
title: "How to: Call Properties and Methods of the Windows Forms Control"
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
ms.topic: get-started-article
ms.assetid: 6e647d8a-fdaa-4aa1-b3fe-04f15cff8eb3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call Properties and Methods of the Windows Forms Control
Because [CWinFormsView::GetControl](../vs140/CWinFormsView--GetControl.md) returns a pointer to <xref:System.Windows.Forms.Control?qualifyHint=True>, and not a pointer to `WindowsControlLibrary1::UserControl1`, it is advisable to add a member of the user control type and initialize it in [IView::OnInitialUpdate](../vs140/IView--OnInitialUpdate.md). Now you can call methods and properties using `m_ViewControl`.  
  
 This topic assumes you have previously completed [How to: Create the User Control and Host in a Dialog Box](../vs140/How-to--Create-the-User-Control-and-Host-in-a-Dialog-Box.md) and [How to: Create the User Control and Host MDI View](../vs140/How-to--Create-the-User-Control-and-Host-MDI-View.md).  
  
### To create the MFC host application  
  
1.  Open the MFC application you created in [How to: Create the User Control and Host MDI View](../vs140/How-to--Create-the-User-Control-and-Host-MDI-View.md).  
  
2.  Add the following line to the public overrides section of the `CMFC02View` class declaration in MFC02View.h.  
  
     `gcroot<WindowsFormsControlLibrary1::UserControl1 ^> m_ViewControl;`  
  
3.  Add an override for OnInitialupdate.  
  
     Display the **Properties** window (F4). In **Class View** (CTRL+SHIFT+C), select CMFC02View class. In the **Properties** window, select the icon for Overrides. Scoll down the list to OnInitialUpdate. Click on the drop down list and select <Add\>. In MFC02View.cpp. make sure the body of the OnInitialUpdate function is as follows:  
  
    ```  
    CWinFormsView::OnInitialUpdate();  
    m_ViewControl = safe_cast<WindowsFormsControlLibrary1::UserControl1 ^>(this->GetControl());  
    m_ViewControl->textBox1->Text = gcnew System::String("hi");  
    ```  
  
4.  Build and run the project.  
  
     On the **Build** menu, click **Build Solution**.  
  
     On the **Debug** menu, click **Start without debugging**.  
  
     Notice that the text box is now initialized.  
  
## See Also  
 [Hosting a Windows Forms User Control as an MFC View](../vs140/Hosting-a-Windows-Forms-User-Control-as-an-MFC-View.md)