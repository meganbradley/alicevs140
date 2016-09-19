---
title: "CTaskDialog::CTaskDialog"
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
ms.assetid: b85933b3-4989-4663-9720-39466e6773d7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::CTaskDialog
Creates an instance of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
## Syntax  
  
```  
CTaskDialog(  
   const CString& strContent,  
   const CString& strMainInstruction,  
   const CString& strTitle,  
   int nCommonButtons = TDCBF_OK_BUTTON | TDCBF_CANCEL_BUTTON,  
   int nTaskDialogOptions = TDF_ENABLE_HYPERLINKS | TDF_USE_COMMAND_LINKS,  
   const CString& strFooter = _T("")  
);  
  
CTaskDialog(  
   const CString& strContent,  
   const CString& strMainInstruction,  
   const CString& strTitle,  
   int nIDCommandControlsFirst,  
   int nIDCommandControlsLast,  
   int nCommonButtons,  
   int nTaskDialogOptions = TDF_ENABLE_HYPERLINKS | TDF_USE_COMMAND_LINKS,  
   const CString& strFooter = _T("")  
);  
```  
  
#### Parameters  
 [in] `strContent`  
 The string to use for the content of the `CTaskDialog`.  
  
 [in] `strMainInstruction`  
 The main instruction of the `CTaskDialog`.  
  
 [in] `strTitle`  
 The title of the `CTaskDialog`.  
  
 [in] `nCommonButtons`  
 A mask of the common buttons to add to the `CTaskDialog`.  
  
 [in] `nTaskDialogOptions`  
 The set of options to use for the `CTaskDialog`.  
  
 [in] `strFooter`  
 The string to use as the footer.  
  
 [in] `nIDCommandControlsFirst`  
 The string ID of the first command.  
  
 [in] `nIDCommandControlsLast`  
 The string ID of the last command.  
  
## Remarks  
 There are two ways that you can add a `CTaskDialog` to your application. The first way is to use one of the constructors to create a `CTaskDialog` and display it using [CTaskDialog::DoModal](../vs140/CTaskDialog--DoModal.md). The second way is to use the static function [CTaskDialog::ShowDialog](../vs140/CTaskDialog--ShowDialog.md), which enables you to display a `CTaskDialog` without explicitly creating a `CTaskDialog` object.  
  
 The second constructor creates command button controls by using data from the resource file of your application. The string table in the resource file has several strings with associated string IDs. This method adds a command button control for each valid entry in the string table between `nIDCommandControlsFirst` and `nCommandControlsLast`, inclusive. For these command button controls, the string in the string table is the control's caption and the string ID is the control's ID.  
  
 See [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md) for a list of valid options.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::ShowDialog](../vs140/CTaskDialog--ShowDialog.md)   
 [CTaskDialog::DoModal](../vs140/CTaskDialog--DoModal.md)   
 [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md)   
 [Walkthrough: Adding a CTaskDialog to an Application](../vs140/Walkthrough--Adding-a-CTaskDialog-to-an-Application.md)