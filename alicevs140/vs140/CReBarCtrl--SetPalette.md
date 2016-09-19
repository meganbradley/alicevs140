---
title: "CReBarCtrl::SetPalette"
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
ms.assetid: e62e8348-3cfc-4c2e-a288-fca442286d9d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetPalette
Implements the behavior of the Win32 message [RB_SETPALETTE](http://msdn.microsoft.com/library/windows/desktop/bb774520), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      CPalette* SetPalette(   
   HPALETTE hPal    
);  
```  
  
#### Parameters  
 *hPal*  
 An `HPALETTE` that specifies the new palette that the rebar control will use.  
  
## Return Value  
 A pointer to a [CPalette](../vs140/CPalette-Class.md) object specifying the rebar control's previous palette.  
  
## Remarks  
 Note that this member function uses a `CPalette` object as its return value, rather than an `HPALETTE`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetPalette](../vs140/CReBarCtrl--GetPalette.md)