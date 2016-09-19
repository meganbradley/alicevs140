---
title: "CRichEditCtrl::SetSelectionCharFormat"
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
ms.assetid: 9e3cfd5d-86f6-4a04-9bfc-740572df997d
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetSelectionCharFormat
Sets the character formatting attributes for the text in the current selection in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      BOOL SetSelectionCharFormat(  
   CHARFORMAT& cf   
);  
BOOL SetSelectionCharFormat(  
   CHARFORMAT2& cf   
);  
```  
  
#### Parameters  
 `cf`  
 In the first version, a pointer to a [CHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb787881) structure containing the new character formatting attributes for the current selection.  
  
 In the second version, a pointer to a [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure, which is a Rich Edit 2.0 extension to the **CHARFORMAT** structure, containing the new character formatting attributes for the current selection.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 Only the attributes specified by the **dwMask** member of `cf` are changed by this function.  
  
 For more information, see the [EM_SETCHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774230) and the **CHARFORMAT** and **CHARFORMAT2** structures in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#31)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetSelectionCharFormat](../vs140/CRichEditCtrl--GetSelectionCharFormat.md)   
 [CRichEditCtrl::SetDefaultCharFormat](../vs140/CRichEditCtrl--SetDefaultCharFormat.md)