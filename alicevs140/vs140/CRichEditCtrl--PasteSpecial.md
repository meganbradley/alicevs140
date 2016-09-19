---
title: "CRichEditCtrl::PasteSpecial"
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
ms.assetid: 758f5360-2f2a-4ebc-93c4-450e9f268181
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::PasteSpecial
Pastes data in a specific Clipboard format into this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      void PasteSpecial(  
   UINT nClipFormat,  
   DWORD dvAspect = 0,  
   HMETAFILE hMF = 0   
);  
```  
  
#### Parameters  
 *nClipFormat*  
 Clipboard format to paste into this `CRichEditCtrl` object.  
  
 *dvAspect*  
 Device aspect for the data to be retrieved from the Clipboard.  
  
 *hMF*  
 Handle to the metafile containing the iconic view of the object to be pasted.  
  
## Remarks  
 The new material is inserted at the insertion point, the location of the caret.  
  
 For more information, see [EM_PASTESPECIAL](http://msdn.microsoft.com/library/windows/desktop/bb774214) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#23)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)   
 [CRichEditCtrl::Copy](../vs140/CRichEditCtrl--Copy.md)   
 [CRichEditCtrl::Cut](../vs140/CRichEditCtrl--Cut.md)