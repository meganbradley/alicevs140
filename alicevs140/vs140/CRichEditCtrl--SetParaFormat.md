---
title: "CRichEditCtrl::SetParaFormat"
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
ms.assetid: a5b4725c-5b2c-43ee-89cd-7bc41f352d9d
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetParaFormat
Sets the paragraph formatting attributes for the current selection in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      BOOL SetParaFormat(  
   PARAFORMAT& pf   
);  
BOOL SetParaFormat(  
   PARAFORMAT2& pf   
);  
```  
  
#### Parameters  
 `pf`  
 In the first version, a pointer to a [PARAFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb787940) structure containing the new default paragraph formatting attributes.  
  
 In the second version, a pointer to a [PARAFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787942) structure, which is a Rich Edit 2.0 extension to the **PARAFORMAT** structure, holding the default character formatting attributes.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 Only the attributes specified by the **dwMask** member of `pf` are changed by this function.  
  
 For more information, see the [EM_SETPARAFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774276) message and the **PARAFORMAT** and **PARAFORMAT2** structures in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#28)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetParaFormat](../vs140/CRichEditCtrl--GetParaFormat.md)   
 [CRichEditCtrl::SetSelectionCharFormat](../vs140/CRichEditCtrl--SetSelectionCharFormat.md)