---
title: "CFileDialog::UpdateOFNFromShellDialog"
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
ms.assetid: bdc75632-bd12-4740-9aeb-17c681f39abc
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::UpdateOFNFromShellDialog
Updates the `m_ofn` data structure of the [CFileDialog](../vs140/CFileDialog-Class.md) based on the current state of the internal object.  
  
## Syntax  
  
```  
void UpdateOFNFromShellDialog();  
```  
  
## Remarks  
 In versions of Windows before [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], the member [OPENFILENAME](https://msdn.microsoft.com/en-us/library/ms911906.aspx) data structure was continuously synchronized with the state of the `CFileDialog`. Any changes to the [m_ofn](../vs140/CFileDialog--m_ofn.md) member variable directly affected the state of the dialog box. Also, any changes to the state of the dialog immediately updated the m_ofn member variable.  
  
 In [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], the `m_ofn` data structure is not automatically updated. To guarantee the accuracy of the data in the `m_ofn` member variable, you should call the `UpdateOFNFromShellDialog` function before accessing the data. Windows calls this function automatically during the processing of [IFileDialog::OnFileOK](http://msdn.microsoft.com/library/windows/desktop/bb775879).  
  
 For more information about how to use the `CFileDialog` class under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Example  
 This example updates the `CFileDialog` before displaying it. Before updating the `m_ofn` member variable, we need to synchronize it to the current state of the dialog box.  
  
 [!CODE [NVC_MFC_CFileDialog#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CFileDialog#1)]  
  
## Requirements  
 `Minimum required operating system:` [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]  
  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::ApplyOFNToShellDialog](../vs140/CFileDialog--ApplyOFNToShellDialog.md)