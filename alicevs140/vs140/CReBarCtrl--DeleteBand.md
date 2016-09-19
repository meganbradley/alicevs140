---
title: "CReBarCtrl::DeleteBand"
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
ms.assetid: 40eaaf5d-3e5d-4dbb-8998-3a4737bd5a23
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::DeleteBand
Implements the behavior of the Win32 message [RB_DELETEBAND](http://msdn.microsoft.com/library/windows/desktop/bb774431), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL DeleteBand(  
   UINT uBand   
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band to be deleted.  
  
## Return Value  
 Nonzero if the band deleted successfully; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#4)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)