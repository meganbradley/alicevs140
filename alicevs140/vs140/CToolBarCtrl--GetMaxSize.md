---
title: "CToolBarCtrl::GetMaxSize"
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
ms.assetid: 3066a413-606a-4af7-b2b7-95f47bc5057b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetMaxSize
Retrieves the total size of all of the visible buttons and separators in the toolbar.  
  
## Syntax  
  
```  
  
      BOOL GetMaxSize(  
   LPSIZE pSize   
) const;  
```  
  
#### Parameters  
 `pSize`  
 A pointer to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure that receives the size of the items.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETMAXSIZE](http://msdn.microsoft.com/library/windows/desktop/bb787341), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)