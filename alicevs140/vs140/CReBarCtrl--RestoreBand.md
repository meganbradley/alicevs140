---
title: "CReBarCtrl::RestoreBand"
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
ms.assetid: 53dd912c-46d9-40bb-a43f-d0d291cf4e2e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::RestoreBand
Resizes a band in a rebar control to its ideal size.  
  
## Syntax  
  
```  
  
      void RestoreBand(  
   UINT uBand  
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band to be maximized.  
  
## Remarks  
 Implements the behavior of the Win32 message [RB_MAXIMIZEBAND](http://msdn.microsoft.com/library/windows/desktop/bb774500) with `fIdeal` set to 1, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::MaximizeBand](../vs140/CReBarCtrl--MaximizeBand.md)   
 [CReBarCtrl::MinimizeBand](../vs140/CReBarCtrl--MinimizeBand.md)