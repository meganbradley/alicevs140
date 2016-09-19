---
title: "CTaskDialog::SetCommonButtonOptions"
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
ms.assetid: 6f9a36e2-41f8-4033-94a5-991a51db2150
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetCommonButtonOptions
Updates a subset of common buttons to be enabled and to require UAC elevation.  
  
## Syntax  
  
```  
void SetCommonButtonOptions(  
   int nDisabledButtonMask,  
   int nElevationButtonMask = 0  
);  
```  
  
#### Parameters  
 [in] `nDisabledButtonMask`  
 A mask for the common buttons to disable.  
  
 [in] `nElevationButtonMask`  
 A mask for the common buttons that require elevation.  
  
## Remarks  
 You can set the common buttons available to an instance of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) by using the constructor [CTaskDialog::CTaskDialog](../vs140/CTaskDialog--CTaskDialog.md) and the method [CTaskDialog::SetCommonButtons](../vs140/CTaskDialog--SetCommonButtons.md). `CTaskDialog::SetCommonButtonOptions` does not support adding new common buttons.  
  
 If you use this method to disable or elevate a common button that is not available for this `CTaskDialog`, this method throws an exception by using the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro.  
  
 This method enables any button that is available to the `CTaskDialog` but is not in the `nDisabledButtonMask`, even if it was previously disabled. This method treats elevation in a similar manner: it records common buttons as not requiring elevation if the common button is available but not included in `nElevationButtonMask`.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#6)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::CTaskDialog](../vs140/CTaskDialog--CTaskDialog.md)   
 [CTaskDialog::SetCommonButtons](../vs140/CTaskDialog--SetCommonButtons.md)