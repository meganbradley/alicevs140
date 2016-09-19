---
title: "CReBarCtrl::SizeToRect"
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
ms.assetid: f0400e75-9dab-47e1-8de3-e88cf6d9077e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SizeToRect
Implements the behavior of the Win32 message [RB_SIZETORECT](http://msdn.microsoft.com/library/windows/desktop/bb774534), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL SizeToRect(  
   CRect& rect   
);  
```  
  
#### Parameters  
 `rect`  
 A reference to a [CRect](../vs140/CRect-Class.md) object that specifies the rectangle that the rebar control should be sized to.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 Note that this member function uses a `CRect` object as a parameter, rather than a `RECT` structure.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetRect](../vs140/CReBarCtrl--GetRect.md)