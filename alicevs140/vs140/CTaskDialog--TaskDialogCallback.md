---
title: "CTaskDialog::TaskDialogCallback"
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
ms.topic: reference
ms.assetid: 64bd1dea-c8c9-4a4e-8f2f-d72ad8cb652f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::TaskDialogCallback
The framework calls this method in response to various Windows messages.  
  
## Syntax  
  
```  
friend:  
HRESULT TaskDialogCallback(  
   HWND hWnd,  
   UINT uNotification,  
   WPARAM wParam,  
   LPARAM lParam,  
   LONG_PTR dwRefData  
);  
```  
  
#### Parameters  
 [in] `hwnd`  
 A handle to the `m_hWnd` structure for the `CTaskDialog`.  
  
 [in] `uNotification`  
 The notification code that specifies the generated message.  
  
 [in] `wParam`  
 More information about the message.  
  
 [in] `lParam`  
 More information about the message.  
  
 [in] `dwRefData`  
 A pointer to the `CTaskDialog` object that the callback message applies to.  
  
## Return Value  
 Depends on the specific notification code. See the Remarks section for more information.  
  
## Remarks  
 The default implementation of `TaskDialogCallback` handles the specific message and then calls the appropriate On method of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md). For example, in response to the `TDN_BUTTON_CLICKED` message, `TaskDialogCallback` calls [CTaskDialog::OnCommandControlClick](../vs140/CTaskDialog--OnCommandControlClick.md).  
  
 The values for `wParam` and `lParam` depend on the specific generated message. It is possible for either or both of these values to be empty. The following table lists the default notifications that are supported and what the values of `wParam` and `lParam` represent. If you override this method in a derived class, you should implement the callback code for each message in the following table.  
  
|Notification Message|`wParam` Value|`lParam` Value|  
|--------------------------|--------------------|--------------------|  
|`TDN_CREATED`|Not used.|Not used.|  
|`TDN_NAVIGATED`|Not used.|Not used.|  
|`TDN_BUTTON_CLICKED`|The command button control ID.|Not used.|  
|`TDN_HYPERLINK_CLICKED`|Not used.|A [LPCWSTR](http://msdn.microsoft.com/library/windows/desktop/aa383751) structure that contains the link.|  
|`TDN_TIMER`|Time in milliseconds since the `CTaskDialog` was created or the timer was reset.|Not used.|  
|`TDN_DESTROYED`|Not used.|Not used.|  
|`TDN_RADIO_BUTTON_CLICKED`|The radio button ID.|Not used.|  
|`TDN_DIALOG_CONSTRUCTED`|Not used.|Not used.|  
|`TDN_VERIFICATION_CLICKED`|1 if the check box is checked, 0 if it is not.|Not used.|  
|`TDN_HELP`|Not used.|Not used.|  
|`TDN_EXPANDO_BUTTON_CLICKED`|0 if the expansion area is collapsed; nonzero if the expansion text is displayed.|Not used.|  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::OnCommandControlClick](../vs140/CTaskDialog--OnCommandControlClick.md)   
 [CTaskDialog::OnCreate](../vs140/CTaskDialog--OnCreate.md)   
 [CTaskDialog::OnDestroy](../vs140/CTaskDialog--OnDestroy.md)   
 [CTaskDialog::OnExpandButtonClick](../vs140/CTaskDialog--OnExpandButtonClick.md)   
 [CTaskDialog::OnHelp](../vs140/CTaskDialog--OnHelp.md)   
 [CTaskDialog::OnHyperlinkClick](../vs140/CTaskDialog--OnHyperlinkClick.md)   
 [CTaskDialog::OnInit](../vs140/CTaskDialog--OnInit.md)   
 [CTaskDialog::OnNavigatePage](../vs140/CTaskDialog--OnNavigatePage.md)   
 [CTaskDialog::OnRadioButtonClick](../vs140/CTaskDialog--OnRadioButtonClick.md)   
 [CTaskDialog::OnTimer](../vs140/CTaskDialog--OnTimer.md)   
 [CTaskDialog::OnVerificationCheckboxClick](../vs140/CTaskDialog--OnVerificationCheckboxClick.md)