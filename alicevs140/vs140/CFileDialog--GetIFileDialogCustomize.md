---
title: "CFileDialog::GetIFileDialogCustomize"
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
ms.assetid: 90ca7c7a-93d8-482c-b509-c9c3fe9c1e47
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetIFileDialogCustomize
Retrieves a pointer to the internal COM object for a given [CFileDialog](../vs140/CFileDialog-Class.md).  
  
## Syntax  
  
```  
IFileDialogCustomize* GetIFileDialogCustomize();  
```  
  
## Return Value  
 The pointer to the internal COM object for the `CFileDialog`. It is your responsibility to release this pointer appropriately.  
  
## Remarks  
 Use this function only under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] with an object that has `bVistaStyle` set to `true`. If you use this function when `bVistaStyle` is `false`, it will return `NULL` in release mode and throw an assertion in debug mode.  
  
 For more information about the `IFileDialogCustomize` interface,  see [IFileDialogCustomize](http://msdn.microsoft.com/library/windows/desktop/bb775912).  
  
## Example  
 This example retrieves the internal COM object. To run this code example, you must compile it under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)].  
  
 [!CODE [NVC_MFC_CFileDialog#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CFileDialog#4)]  
  
## Requirements  
 **Minimum required operating system:** [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]  
  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetIFileOpenDialog](../vs140/CFileDialog--GetIFileOpenDialog.md)   
 [CFileDialog::GetIFileSaveDialog](../vs140/CFileDialog--GetIFileSaveDialog.md)