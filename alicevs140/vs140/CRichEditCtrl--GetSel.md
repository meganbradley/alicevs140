---
title: "CRichEditCtrl::GetSel"
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
ms.assetid: 9d487125-c79d-4ff3-bcff-d93d14715a0a
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetSel
Retrieves the bounds of the current selection in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      void GetSel(  
   CHARRANGE& cr   
) const;  
void GetSel(  
   long& nStartChar,  
   long& nEndChar   
) const;  
```  
  
#### Parameters  
 `cr`  
 Reference to a [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure to receive the bounds of the current selection.  
  
 `nStartChar`  
 Zero-based index of the first character in the current selection.  
  
 `nEndChar`  
 Zero-based index of the last character in the current selection.  
  
## Remarks  
 The two forms of this function provide alternate ways to get the bounds for the selection. Brief descriptions of these forms follow:  
  
-   **GetSel(**  `cr`  **)** This form uses the **CHARRANGE** structure with its **cpMin** and **cpMax** members to return the bounds.  
  
-   **GetSel(**  `nStartChar` **,**  `nEndChar`  **)** This form returns the bounds in the parameters `nStartChar` and `nEndChar`.  
  
 The selection includes everything if the beginning (**cpMin** or `nStartChar`) is 0 and the end (**cpMax** or `nEndChar`) is – 1.  
  
 For more information, see [EM_EXGETSEL](http://msdn.microsoft.com/library/windows/desktop/bb788001) message and [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetSel](../vs140/CRichEditCtrl--SetSel.md)   
 [CRichEditCtrl::GetSelText](../vs140/CRichEditCtrl--GetSelText.md)   
 [CRichEditCtrl::GetParaFormat](../vs140/CRichEditCtrl--GetParaFormat.md)   
 [CRichEditCtrl::GetSelectionCharFormat](../vs140/CRichEditCtrl--GetSelectionCharFormat.md)