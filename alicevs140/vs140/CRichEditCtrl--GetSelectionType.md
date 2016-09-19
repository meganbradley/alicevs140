---
title: "CRichEditCtrl::GetSelectionType"
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
ms.assetid: 527e2f24-4b82-4b61-ae98-616a48aeec87
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetSelectionType
Determines the selection type in this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
WORD GetSelectionType( ) const;  
  
```  
  
## Return Value  
 Flags indicating the contents of the current selection. A combination of the following flags:  
  
-   `SEL_EMPTY` Indicates that there is no current selection.  
  
-   `SEL_TEXT` Indicates that the current selection contains text.  
  
-   `SEL_OBJECT` Indicates that the current selection contains at least one OLE item.  
  
-   `SEL_MULTICHAR` Indicates that the current selection contains more than one character of text.  
  
-   `SEL_MULTIOBJECT` Indicates that the current selection contains more than one OLE object.  
  
## Remarks  
 For more information, see [EM_SELECTIONTYPE](http://msdn.microsoft.com/library/windows/desktop/bb774223) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#16)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetSel](../vs140/CRichEditCtrl--GetSel.md)   
 [CRichEditCtrl::GetSelText](../vs140/CRichEditCtrl--GetSelText.md)