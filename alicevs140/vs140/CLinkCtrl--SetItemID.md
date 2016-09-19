---
title: "CLinkCtrl::SetItemID"
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
ms.assetid: e1747f43-985d-4636-a019-c59364c51c3f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::SetItemID
Retrieves the ID of a link control item.  
  
## Syntax  
  
```  
  
      BOOL SetItemID(  
   int iLink,  
   LPCWSTR szID   
);  
```  
  
#### Parameters  
 `iLink`  
 The index of a link control item.  
  
 *szID*  
 A null-terminated string containing the ID of the specified item.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 Sets the ID of a specific link control item. For more information, see the Win32 message [LM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760724) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::GetItemID](../vs140/CLinkCtrl--GetItemID.md)   
 [CLinkCtrl::GetItem](../vs140/CLinkCtrl--GetItem.md)