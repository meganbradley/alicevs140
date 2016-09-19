---
title: "CListCtrl::SetInfoTip"
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
ms.assetid: 7d169820-b661-440f-a736-9a8aaf7ea9a1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetInfoTip
Sets the tooltip text.  
  
## Syntax  
  
```  
  
      BOOL SetInfoTip(  
   PLVSETINFOTIP plvInfoTip   
);  
```  
  
#### Parameters  
 *plvInfoTip*  
 A pointer to an [LVFSETINFOTIP](http://msdn.microsoft.com/library/windows/desktop/bb774764) structure containing the information to be set.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETINFOTIP](http://msdn.microsoft.com/library/windows/desktop/bb761180) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)