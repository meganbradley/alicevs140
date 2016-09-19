---
title: "CRichEditCtrl::SetReadOnly"
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
ms.assetid: 3fd897a6-ec1c-487a-8e44-b77a9a7c8ccb
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetReadOnly
Changes the `ECO_READONLY` option for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      BOOL SetReadOnly(  
   BOOL bReadOnly = TRUE   
);  
```  
  
#### Parameters  
 `bReadOnly`  
 Indicates if this `CRichEditCtrl` object should be read only.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 For a brief description of this option, see [SetOptions](../vs140/CRichEditCtrl--SetOptions.md). You can use this function to set all the options for this `CRichEditCtrl` object.  
  
 For more information, see [EM_SETREADONLY](http://msdn.microsoft.com/library/windows/desktop/bb761655) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#29)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Create](../vs140/CRichEditCtrl--Create.md)   
 [CRichEditCtrl::SetOptions](../vs140/CRichEditCtrl--SetOptions.md)