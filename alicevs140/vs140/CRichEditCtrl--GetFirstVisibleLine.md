---
title: "CRichEditCtrl::GetFirstVisibleLine"
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
ms.assetid: 55d1d9b7-a76a-44d7-9bc4-ca4f729f0fff
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetFirstVisibleLine
Determines the topmost visible line in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
int GetFirstVisibleLine( ) const;  
  
```  
  
## Return Value  
 Zero-based index of the uppermost visible line in this `CRichEditCtrl` object.  
  
## Remarks  
 For more information, see [EM_GETFIRSTVISIBLELINE](http://msdn.microsoft.com/library/windows/desktop/bb761574) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#11)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetLine](../vs140/CRichEditCtrl--GetLine.md)   
 [CRichEditCtrl::GetLineCount](../vs140/CRichEditCtrl--GetLineCount.md)