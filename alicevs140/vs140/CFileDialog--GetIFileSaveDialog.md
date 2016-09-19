---
title: "CFileDialog::GetIFileSaveDialog"
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
ms.assetid: 2c1882bc-0692-40d9-81ba-ec02cd733c31
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetIFileSaveDialog
Retrieves a pointer to the internal COM object for a given `CFileDialog`.  
  
## Syntax  
  
```  
IFileSaveDialog* GetIFileSaveDialog();  
```  
  
## Return Value  
 The pointer to the internal COM object for the `CFileDialog`. It is your responsibility to release this pointer appropriately.  
  
## Remarks  
 Use this function only under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] with an object that has `bVistaStyle` set to `true`. This function will return `NULL` if the `CFileDialog` is not a **Save** dialog box or if `bVistaStyle` is set to `false`. In this final case, the function only returns `NULL` in release mode - in debug mode it will throw an assertion.  
  
 For more information about the `IFileSaveDialog` interface, see [IFileSaveDialog](http://msdn.microsoft.com/library/windows/desktop/bb775688).  
  
## Example  
 This example retrieves the internal COM object. To run this code example, you must compile it under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)].  
  
 [!CODE [NVC_MFC_CFileDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CFileDialog#3)]  
  
## Requirements  
 `Minimum required operating system:` [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]  
  
 `Header:` afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetIFileDialogCustomize](../vs140/CFileDialog--GetIFileDialogCustomize.md)   
 [CFileDialog::GetIFileOpenDialog](../vs140/CFileDialog--GetIFileOpenDialog.md)