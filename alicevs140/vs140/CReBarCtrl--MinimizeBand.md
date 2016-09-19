---
title: "CReBarCtrl::MinimizeBand"
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
ms.assetid: 0f5bdb84-abb4-4fb3-89de-0c674eaf0241
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::MinimizeBand
Resizes a band in a rebar control to its smallest size.  
  
## Syntax  
  
```  
  
      void MinimizeBand(  
   UINT uBand   
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band to be minimized.  
  
## Remarks  
 Implements the behavior of the Win32 message [RB_MINIMIZEBAND](http://msdn.microsoft.com/library/windows/desktop/bb774502), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#11)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::MaximizeBand](../vs140/CReBarCtrl--MaximizeBand.md)