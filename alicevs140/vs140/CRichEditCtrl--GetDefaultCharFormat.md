---
title: "CRichEditCtrl::GetDefaultCharFormat"
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
ms.assetid: 0c862a43-b47d-48a9-a7a9-c5e86e6ab826
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetDefaultCharFormat
Gets the default character formatting attributes of this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      DWORD GetDefaultCharFormat(  
   CHARFORMAT& cf   
) const;  
DWORD GetDefaultCharFormat(  
   CHARFORMAT2& cf   
) const;  
```  
  
#### Parameters  
 `cf`  
 In the first version, a pointer to a **CHARFORMAT** structure holding the default character formatting attributes.  
  
 In the second version, a pointer to a **CHARFORMAT2** structure, which is a Rich Edit 2.0 extension to the **CHARFORMAT** structure, holding the default character formatting attributes.  
  
## Return Value  
 The **dwMask** data member of `cf`. It specified the default character formatting attributes.  
  
## Remarks  
 For more information, see the **EM_GETCHARFORMAT** message and the **CHARFORMAT** and **CHARFORMAT2** structures in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [SetDefaultCharFormat](../vs140/CRichEditCtrl--SetDefaultCharFormat.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetDefaultCharFormat](../vs140/CRichEditCtrl--SetDefaultCharFormat.md)   
 [CRichEditCtrl::GetSelectionCharFormat](../vs140/CRichEditCtrl--GetSelectionCharFormat.md)   
 [CRichEditCtrl::GetParaFormat](../vs140/CRichEditCtrl--GetParaFormat.md)