---
title: "CRichEditCtrl::FormatRange"
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
ms.assetid: 015661ef-66c9-408e-bc91-026165dbfa5a
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::FormatRange
Formats a range of text in a rich edit control for a specific device.  
  
## Syntax  
  
```  
  
      long FormatRange(  
   FORMATRANGE* pfr,  
   BOOL bDisplay = TRUE   
);  
```  
  
#### Parameters  
 *pfr*  
 Pointer to the [FORMATRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787911) structure which contains information about the output device. **NULL** indicates that cached information within the rich edit control can be freed.  
  
 *bDisplay*  
 Indicates if the text should be rendered. If **FALSE**, the text is just measured.  
  
## Return Value  
 The index of the last character that fits in the region plus one.  
  
## Remarks  
 Typically, this call is followed by a call to [DisplayBand](../vs140/CRichEditCtrl--DisplayBand.md).  
  
 For more information, see [EM_FORMATRANGE](http://msdn.microsoft.com/library/windows/desktop/bb788020) message and [FORMATRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787911) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::DisplayBand](../vs140/CRichEditCtrl--DisplayBand.md)