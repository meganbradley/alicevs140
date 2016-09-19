---
title: "CFileDialog::GetReadOnlyPref"
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
ms.assetid: 4611071d-b24f-4c0d-bd93-bdde30200ee4
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetReadOnlyPref
Call this function to determine whether the Read Only check box has been selected in the Windows standard File Open and File Save As dialog boxes.  
  
## Syntax  
  
```  
BOOL GetReadOnlyPref( ) const;  
```  
  
## Return Value  
 Non-zero if the Read Only check box in the dialog box is selected; otherwise 0.  
  
## Remarks  
 You can hide the Read Only check box by setting the `OFN_HIDEREADONLY` style in the [CFileDialog](../vs140/CFileDialog-Class.md) constructor.  
  
> [!NOTE]
>  [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] style `CFileDialog` objects do not support this function. Attempting to use this function on a [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] style `CFileDialog` will throw [CNotSupportedException](../vs140/CNotSupportedException-Class.md). See [CFileDialog Class](../vs140/CFileDialog-Class.md) for more information.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::CFileDialog](../vs140/CFileDialog--CFileDialog.md)   
 [CFileDialog::GetPathName](../vs140/CFileDialog--GetPathName.md)   
 [CFileDialog::GetFileExt](../vs140/CFileDialog--GetFileExt.md)