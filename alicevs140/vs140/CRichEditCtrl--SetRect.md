---
title: "CRichEditCtrl::SetRect"
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
ms.assetid: 75c959ae-c11e-4e94-a1ff-b5f8259393a6
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetRect
Sets the formatting rectangle for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      void SetRect(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 [CRect](../vs140/CRect-Class.md) or pointer to a [RECT](../vs140/RECT-Structure.md) that indicates the new bounds for the formatting rectangle.  
  
## Remarks  
 The formatting rectangle is the limiting rectangle for the text. The limiting rectangle is independent of the size of the rich edit control window. When this `CRichEditCtrl` object is first created, the formatting rectangle is the same size as the client area of the window. Use `SetRect` to make the formatting rectangle larger or smaller than the rich edit window.  
  
 For more information, see [EM_SETRECT](http://msdn.microsoft.com/library/windows/desktop/bb761657) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#30)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetRect](../vs140/CRichEditCtrl--GetRect.md)