---
title: "CReBarCtrl::GetPalette"
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
ms.assetid: d97afabf-79fb-4cfb-ae26-2c5c63c47fc8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetPalette
Retrieves the rebar control's current palette.  
  
## Syntax  
  
```  
  
CPalette* GetPalette( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CPalette](../vs140/CPalette-Class.md) object specifying the rebar control's current palette.  
  
## Remarks  
 Note that this member function uses a `CPalette` object as its return value, rather than an `HPALETTE`.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::SetPalette](../vs140/CReBarCtrl--SetPalette.md)