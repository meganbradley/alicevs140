---
title: "CTaskDialog::SetDefaultCommandControl"
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
ms.assetid: 17afe828-8525-4c2c-a503-c162a1df000c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetDefaultCommandControl
Specifies the default command button control.  
  
## Syntax  
  
```  
void SetDefaultCommandControl(  
   int nCommandControlID  
);  
```  
  
#### Parameters  
 [in] `nCommandControlID`  
 The ID of the command button control to be the default.  
  
## Remarks  
 The default command button control is the control that is selected when the `CTaskDialog` is first displayed to the user.  
  
 This method throws an exception if it cannot find the command button control specified by `nCommandControlID`.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#2)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddCommandControl](../vs140/CTaskDialog--AddCommandControl.md)   
 [CTaskDialog::SetCommandControlOptions](../vs140/CTaskDialog--SetCommandControlOptions.md)   
 [CTaskDialog::GetSelectedCommandControlID](../vs140/CTaskDialog--GetSelectedCommandControlID.md)   
 [CTaskDialog::IsCommandControlEnabled](../vs140/CTaskDialog--IsCommandControlEnabled.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)