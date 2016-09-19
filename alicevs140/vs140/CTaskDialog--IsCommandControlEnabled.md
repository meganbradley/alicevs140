---
title: "CTaskDialog::IsCommandControlEnabled"
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
ms.assetid: d4a45967-57f0-41fd-b013-206a70a868a8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::IsCommandControlEnabled
Determines whether a command button control or button is enabled.  
  
## Syntax  
  
```  
BOOL IsCommandControlEnabled(  
   int nCommandControlID  
) const;  
```  
  
#### Parameters  
 [in] `nCommandControlID`  
 The ID of the command button control or button to test.  
  
## Return Value  
 `TRUE` if the control is enabled, `FALSE` if it is not.  
  
## Remarks  
 You can use this method to determine the availability of both command button controls and the common buttons of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
 If `nCommandControlID` is not a valid identifier for either a common `CTaskDialog` button or a command button control, this method throws an exception.  
  
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
 [CTaskDialog::SetDefaultCommandControl](../vs140/CTaskDialog--SetDefaultCommandControl.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)