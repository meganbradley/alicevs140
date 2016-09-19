---
title: "CReBarCtrl::MaximizeBand"
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
ms.assetid: 340183f7-3976-43ed-b935-4d53ecd63eba
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::MaximizeBand
Resizes a band in a rebar control to its largest size.  
  
## Syntax  
  
```  
  
      void MaximizeBand(  
   UINT uBand   
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band to be maximized.  
  
## Remarks  
 Implements the behavior of the Win32 message [RB_MAXIMIZEBAND](http://msdn.microsoft.com/library/windows/desktop/bb774500) with `fIdeal` set to 0, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::MinimizeBand](../vs140/CReBarCtrl--MinimizeBand.md)   
 [CReBarCtrl::RestoreBand](../vs140/CReBarCtrl--RestoreBand.md)