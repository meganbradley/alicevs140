---
title: "CTaskDialog::AddCommandControl"
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
ms.assetid: 297c4c0a-419e-49f8-8963-af938ed6eb10
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::AddCommandControl
Adds a new command button control to the `CTaskDialog`.  
  
## Syntax  
  
```  
void AddCommandControl(  
   int nCommandControlID,  
   const CString& strCaption,  
   BOOL bEnabled = TRUE,  
   BOOL bRequiresElevation = FALSE  
);  
```  
  
#### Parameters  
 [in] `nCommandControlID`  
 The command control identification number.  
  
 [in] `strCaption`  
 The string that the `CTaskDialog` displays to the user. Use this string to explain the purpose of the command.  
  
 [in] `bEnabled`  
 A Boolean parameter that indicates if the new button is enabled or disabled.  
  
 [in] `bRequiresElevation`  
 A Boolean parameter that indicates whether a command requires elevation.  
  
## Remarks  
 The [CTaskDialog Class](../vs140/CTaskDialog-Class.md) can display an unlimited number of command button controls. However, if a `CTaskDialog` displays any command button controls, it can display a maximum of six buttons. If a `CTaskDialog` has no command button controls, it can display an unlimited number of buttons.  
  
 When the user selects a command button control, the `CTaskDialog` closes. If your application displays the dialog box by using [CTaskDialog::DoModal](../vs140/CTaskDialog--DoModal.md), `DoModal` returns the `nCommandControlID` of the selected command button control.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#2)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::ClickCommandControl](../vs140/CTaskDialog--ClickCommandControl.md)   
 [CTaskDialog::GetSelectedCommandControlID](../vs140/CTaskDialog--GetSelectedCommandControlID.md)   
 [CTaskDialog::IsCommandControlEnabled](../vs140/CTaskDialog--IsCommandControlEnabled.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)   
 [CTaskDialog::SetCommandControlOptions](../vs140/CTaskDialog--SetCommandControlOptions.md)   
 [CTaskDialog::SetDefaultCommandControl](../vs140/CTaskDialog--SetDefaultCommandControl.md)