---
title: "CToolBarCtrl::GetBitmap"
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
ms.assetid: 193b5690-887f-4f40-b88f-078b90cf3dec
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetBitmap
Retrieves the index of the bitmap associated with a button in a toolbar.  
  
## Syntax  
  
```  
  
      int GetBitmap(  
   int nID  
) const;  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button whose bitmap index is to be retrieved.  
  
## Return Value  
 Returns the index of the bitmap if successful, or zero otherwise.  
  
## Remarks  
 Implements the functionality of [TB_GETBITMAP](http://msdn.microsoft.com/library/windows/desktop/bb787315) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)