---
title: "CRichEditCtrl::SetEventMask"
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
ms.assetid: 7d5c1ae5-f7ed-40f4-8c98-0ff1803a7e77
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetEventMask
Sets the event mask for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      DWORD SetEventMask(  
   DWORD dwEventMask   
);  
```  
  
#### Parameters  
 *dwEventMask*  
 The new event mask for this `CRichEditCtrl` object.  
  
## Return Value  
 The previous event mask.  
  
## Remarks  
 The event mask specifies which notification messages the `CRichEditCtrl` object sends to its parent window.  
  
 For more information, see [EM_SETEVENTMASK](http://msdn.microsoft.com/library/windows/desktop/bb774238) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#26)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetEventMask](../vs140/CRichEditCtrl--GetEventMask.md)