---
title: "CTaskDialog::LoadCommandControls"
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
ms.assetid: 8a321702-82b0-469b-8500-00bd6b6f06e8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::LoadCommandControls
Adds command button controls by using data from the string table.  
  
## Syntax  
  
```  
void LoadCommandControls(  
   int nIDCommandControlsFirst,  
   int nIDCommandControlsLast  
);  
```  
  
#### Parameters  
 [in] `nIDCommandControlsFirst`  
 The string ID of the first command.  
  
 [in] `nIDCommandControlsLast`  
 The string ID of the last command.  
  
## Remarks  
 This method creates command button controls by using data from the resource file of your application. The string table in the resource file has several strings with associated string IDs. New command button controls added by using this method use the string for the control's caption and the string ID for the control's ID. The range of strings selected is provided by `nIDCommandControlsFirst` and `nCommandControlsLast`, inclusive. If there is an empty entry in the range, the method does not add a command button control for that entry.  
  
 By default, new command button controls are enabled and do not require elevation.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#2)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddCommandControl](../vs140/CTaskDialog--AddCommandControl.md)   
 [CTaskDialog::SetCommandControlOptions](../vs140/CTaskDialog--SetCommandControlOptions.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)