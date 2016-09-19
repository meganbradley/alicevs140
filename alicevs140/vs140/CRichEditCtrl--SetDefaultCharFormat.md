---
title: "CRichEditCtrl::SetDefaultCharFormat"
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
ms.assetid: 5dafbd8b-d4a2-45b4-be43-f115a799d96e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetDefaultCharFormat
Sets the character formatting attributes for new text in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      BOOL SetDefaultCharFormat(  
   CHARFORMAT& cf   
);  
BOOL SetDefaultCharFormat(  
   CHARFORMAT2& cf   
);  
```  
  
#### Parameters  
 `cf`  
 In the first version, a pointer to a [CHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb787881) structure containing the new default character formatting attributes.  
  
 In the second version, a pointer to a [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure, which is a Rich Edit 2.0 extension to the **CHARFORMAT** structure, containing the default character formatting attributes.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 Only the attributes specified by the **dwMask** member of `cf` are changed by this function.  
  
 For more information, see the [EM_SETCHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774230) message and the **CHARFORMAT** and **CHARFORMAT2** structures in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#25)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetDefaultCharFormat](../vs140/CRichEditCtrl--GetDefaultCharFormat.md)   
 [CRichEditCtrl::SetSelectionCharFormat](../vs140/CRichEditCtrl--SetSelectionCharFormat.md)