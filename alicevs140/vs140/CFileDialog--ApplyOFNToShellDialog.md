---
title: "CFileDialog::ApplyOFNToShellDialog"
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
ms.assetid: bc3ab486-a5b6-4e98-875d-ba499975a996
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::ApplyOFNToShellDialog
Updates the current state of the [CFileDialog](../vs140/CFileDialog-Class.md) based on the values stored in the `m_ofn` data structure.  
  
## Syntax  
  
```  
void ApplyOFNToShellDialog();  
```  
  
## Remarks  
 In versions of Windows before [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], the member [OPENFILENAME](https://msdn.microsoft.com/en-us/library/ms911906.aspx) data structure was continuously synchronized with the state of the `CFileDialog`. Any changes to the [m_ofn](../vs140/CFileDialog--m_ofn.md) member variable were immediately reflected in the state of the dialog box. Also, any changes to the state of the dialog box immediately update the `m_ofn` member variable.  
  
 In [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], the values in the `m_ofn` member variable and state of the `CFileDialog` are not guaranteed to be synchronized. This function forces the state of the `CFileDialog` to be updated to match the `m_ofn` structure. Windows calls this function automatically during [CFileDialog::DoModal](../vs140/CFileDialog--DoModal.md).  
  
 For more information about how to use the `CFileDialog` class under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Example  
 See the example for [CFileDialog::UpdateOFNFromShellDialog](../vs140/CFileDialog--UpdateOFNFromShellDialog.md).  
  
## Requirements  
 **Minimum required operating system:** [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]  
  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::UpdateOFNFromShellDialog](../vs140/CFileDialog--UpdateOFNFromShellDialog.md)