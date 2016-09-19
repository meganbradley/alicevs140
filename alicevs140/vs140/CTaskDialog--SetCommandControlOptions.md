---
title: "CTaskDialog::SetCommandControlOptions"
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
ms.assetid: 796f2e82-2db5-4d5c-88f3-c0ea3483f0b3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetCommandControlOptions
Updates a command button control on the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetCommandControlOptions(  
   int nCommandControlID,  
   BOOL bEnabled,  
   BOOL bRequiresElevation = FALSE  
);  
```  
  
#### Parameters  
 [in] `nCommandControlID`  
 The ID of the command control to update.  
  
 [in] `bEnabled`  
 A Boolean parameter that indicates if the specified command button control is enabled or disabled.  
  
 [in] `bRequiresElevation`  
 A Boolean parameter that indicates if the specified command button control requires elevation.  
  
## Remarks  
 Use this method to change whether a command button control is enabled or requires elevation after it has been added to the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#2)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddCommandControl](../vs140/CTaskDialog--AddCommandControl.md)   
 [CTaskDialog::ClickCommandControl](../vs140/CTaskDialog--ClickCommandControl.md)   
 [CTaskDialog::GetSelectedCommandControlID](../vs140/CTaskDialog--GetSelectedCommandControlID.md)   
 [CTaskDialog::IsCommandControlEnabled](../vs140/CTaskDialog--IsCommandControlEnabled.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)   
 [CTaskDialog::SetDefaultCommandControl](../vs140/CTaskDialog--SetDefaultCommandControl.md)