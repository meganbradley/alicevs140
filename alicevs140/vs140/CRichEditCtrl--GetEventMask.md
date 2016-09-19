---
title: "CRichEditCtrl::GetEventMask"
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
ms.assetid: 05345be6-e4cd-4106-81a8-92803f31459a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetEventMask
Gets the event mask for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
long GetEventMask( ) const;  
  
```  
  
## Return Value  
 The event mask for this `CRichEditCtrl` object.  
  
## Remarks  
 The event mask specifies which notification messages the `CRichEditCtrl` object sends to its parent window.  
  
 For more information, see [EM_GETEVENTMASK](http://msdn.microsoft.com/library/windows/desktop/bb788032) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CRichEditCtrl::SetEventMask](../vs140/CRichEditCtrl--SetEventMask.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetEventMask](../vs140/CRichEditCtrl--SetEventMask.md)   
 [CRichEditCtrl::CRichEditCtrl](../vs140/CRichEditCtrl--CRichEditCtrl.md)