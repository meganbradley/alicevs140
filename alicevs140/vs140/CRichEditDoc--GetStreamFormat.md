---
title: "CRichEditDoc::GetStreamFormat"
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
ms.assetid: 0c3c3c3e-f41c-416d-9041-ee6cc1873566
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditDoc::GetStreamFormat
Call this function to determine the text format for streaming the contents of the rich edit.  
  
## Syntax  
  
```  
  
int GetStreamFormat( ) const;  
  
```  
  
## Return Value  
 One of the following flags:  
  
-   `SF_TEXT` Indicates that the rich edit control does not maintain formatting information.  
  
-   `SF_RTF` Indicates that the rich edit control does maintain formatting information.  
  
## Remarks  
 The return value is based on the [m_bRTF](../vs140/CRichEditDoc--m_bRTF.md) data member. This function returns `SF_RTF` if `m_bRTF` is **TRUE**; otherwise, `SF_TEXT`.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditDoc Class](../vs140/CRichEditDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditDoc::m_bRTF](../vs140/CRichEditDoc--m_bRTF.md)   
 [CRichEditCtrl::StreamIn](../vs140/CRichEditCtrl--StreamIn.md)   
 [CRichEditCtrl::StreamOut](../vs140/CRichEditCtrl--StreamOut.md)