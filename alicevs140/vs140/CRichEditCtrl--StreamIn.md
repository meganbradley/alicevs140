---
title: "CRichEditCtrl::StreamIn"
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
ms.assetid: baf64564-584d-43f4-9796-347880257244
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::StreamIn
Replaces text in this `CRichEditCtrl` object with text from the specified input stream.  
  
## Syntax  
  
```  
  
      long StreamIn(  
   int nFormat,  
   EDITSTREAM& es   
);  
```  
  
#### Parameters  
 `nFormat`  
 Flags specifying the input data formats. See the Remarks section for more information.  
  
 `es`  
 [EDITSTREAM](http://msdn.microsoft.com/library/windows/desktop/bb787891) structure specifying the input stream. See the Remarks section for more information.  
  
## Return Value  
 Number of characters read from the input stream.  
  
## Remarks  
 The value of `nFormat` must be one of the following:  
  
-   `SF_TEXT` Indicates reading text only.  
  
-   `SF_RTF` Indicates reading text and formatting.  
  
 Either of these values can be combined with `SFF_SELECTION`. If `SFF_SELECTION` is specified, `StreamIn` replaces the current selection with the contents of the input stream. If it is not specified, `StreamIn` replaces the entire contents of this `CRichEditCtrl` object.  
  
 In the **EDITSTREAM** parameter `es`, you specify a callback function that fills a buffer with text. This callback function is called repeatedly, until the input stream is exhausted.  
  
 For more information, see [EM_STREAMIN](http://msdn.microsoft.com/library/windows/desktop/bb774302) message and [EDITSTREAM](http://msdn.microsoft.com/library/windows/desktop/bb787891) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#34)]  
  
 [!CODE [NVC_MFC_CRichEditCtrl#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#35)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::StreamOut](../vs140/CRichEditCtrl--StreamOut.md)