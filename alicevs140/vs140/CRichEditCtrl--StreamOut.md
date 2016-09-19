---
title: "CRichEditCtrl::StreamOut"
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
ms.assetid: 8f60cd95-f368-4a0d-8c9c-12160dcdb0eb
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::StreamOut
Writes out the contents of this `CRichEditCtrl` object to the specified output stream.  
  
## Syntax  
  
```  
  
      long StreamOut(  
   int nFormat,  
   EDITSTREAM& es   
);  
```  
  
#### Parameters  
 `nFormat`  
 Flags specifying the output data formats. See the Remarks section for more information.  
  
 `es`  
 [EDITSTREAM](http://msdn.microsoft.com/library/windows/desktop/bb787891) structure specifying the output stream. See the Remarks section for more information.  
  
## Return Value  
 Number of characters written to the output stream.  
  
## Remarks  
 The value of `nFormat` must be one of the following:  
  
-   `SF_TEXT` Indicates writing text only.  
  
-   `SF_RTF` Indicates writing text and formatting.  
  
-   `SF_RTFNOOBJS` Indicates writing text and formatting, replacing OLE items with spaces.  
  
-   `SF_TEXTIZED` Indicates writing text and formatting, with textual representations of OLE items.  
  
 Any of these values can be combined with `SFF_SELECTION`. If `SFF_SELECTION` is specified, `StreamOut` writes out the current selection into the output stream. If it is not specified, `StreamOut` writes out the entire contents of this `CRichEditCtrl` object.  
  
 In the **EDITSTREAM** parameter `es`, you specify a callback function which fills a buffer with text. This callback function is called repeatedly, until the output stream is exhausted.  
  
 For more information, see [EM_STREAMOUT](http://msdn.microsoft.com/library/windows/desktop/bb774304) message and [EDITSTREAM](http://msdn.microsoft.com/library/windows/desktop/bb787891) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#36)]  
  
 [!CODE [NVC_MFC_CRichEditCtrl#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#37)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::StreamIn](../vs140/CRichEditCtrl--StreamIn.md)