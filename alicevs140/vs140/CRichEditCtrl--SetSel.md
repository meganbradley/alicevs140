---
title: "CRichEditCtrl::SetSel"
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
ms.assetid: cd42a64b-aa18-44a0-ad1e-2375dc207f47
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetSel
Sets the selection within this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      void SetSel(  
   long nStartChar,  
   long nEndChar   
);  
void SetSel(  
   CHARRANGE& cr   
);  
```  
  
#### Parameters  
 `nStartChar`  
 Zero-based index of the first character for the selection.  
  
 `nEndChar`  
 Zero-based index of the last character for the selection.  
  
 `cr`  
 [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure which holds the bounds of the current selection.  
  
## Remarks  
 The two forms of this function provide alternate ways to set the bounds for the selection. Brief descriptions of these forms follow:  
  
-   **SetSel(**  `cr`  **)** This form uses the **CHARRANGE** structure with its **cpMin** and **cpMax** members to set the bounds.  
  
-   **SetSel(**  `nStartChar` **,**  `nEndChar`  **)** This form use the parameters `nStartChar` and `nEndChar` to set the bounds.  
  
 The caret is placed at the end of the selection indicated by the greater of the start (**cpMin** or `nStartChar`) and end (**cpMax** or `nEndChar`) indices. This function scrolls the contents of the `CRichEditCtrl` so that the caret is visible.  
  
 To select all the text in this `CRichEditCtrl` object, call `SetSel` with a start index of 0 and an end index of – 1.  
  
 For more information, see [EM_EXSETSEL](http://msdn.microsoft.com/library/windows/desktop/bb788007) message and [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [GetSel](../vs140/CRichEditCtrl--GetSel.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetSel](../vs140/CRichEditCtrl--GetSel.md)   
 [CRichEditCtrl::GetSelectionType](../vs140/CRichEditCtrl--GetSelectionType.md)