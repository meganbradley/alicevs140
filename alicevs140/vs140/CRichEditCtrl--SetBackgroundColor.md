---
title: "CRichEditCtrl::SetBackgroundColor"
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
ms.assetid: e5f071de-fe4c-4fd3-8e2b-47a302d3a2d4
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetBackgroundColor
Sets the background color for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      COLORREF SetBackgroundColor(  
   BOOL bSysColor,  
   COLORREF cr   
);  
```  
  
#### Parameters  
 `bSysColor`  
 Indicates if the background color should be set to the system value. If this value is **TRUE**, `cr` is ignored.  
  
 `cr`  
 The requested background color. Used only if `bSysColor` is **FALSE**.  
  
## Return Value  
 The previous background color for this `CRichEditCtrl` object.  
  
## Remarks  
 The background color can be set to the system value or to a specified [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value.  
  
 For more information, see [EM_SETBKGNDCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb774228) message and [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#24)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetBkColor](../vs140/CDC--SetBkColor.md)