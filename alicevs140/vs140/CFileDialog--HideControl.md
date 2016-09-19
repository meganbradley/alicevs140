---
title: "CFileDialog::HideControl"
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
ms.assetid: aeaf7976-53e7-4167-ba9b-00d9304de343
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::HideControl
Call this member function to hide the specified control in an Explorer-style Open or Save As common dialog box.  
  
## Syntax  
  
```  
  
      void HideControl(  
   int nID   
);  
```  
  
#### Parameters  
 `nID`  
 The ID of the control to hide.  
  
## Remarks  
 The dialog box must have been created with the **OFN_EXPLORER** style; otherwise, the function will fail with an assertion.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDM_HIDECONTROL](http://msdn.microsoft.com/library/windows/desktop/ms646853)   
 [CFileDialog::SetControlText](../vs140/CFileDialog--SetControlText.md)