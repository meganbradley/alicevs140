---
title: "CLinkCtrl::GetItemID"
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
ms.assetid: df597f09-62ef-4189-bbe0-2ada8c486bd3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::GetItemID
Retrieves the ID of a link control item.  
  
## Syntax  
  
```  
  
      BOOL GetItemID(  
   int iLink,  
   CString& strID   
) const;  
BOOL GetItemID(  
   int iLink,  
   LPWSTR szID,  
   UINT cchID   
) const;  
```  
  
#### Parameters  
 `iLink`  
 The index of a link control item.  
  
 *strID*  
 A [CStringT](../vs140/CStringT-Class.md) object containing the ID of the specified item.  
  
 *szID*  
 A null-terminated string containing the ID of the specified item.  
  
 *cchID*  
 The size in characters of the *szID* buffer.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
> [!NOTE]
>  This function also returns **FALSE** if the buffer of *szID or strID* is smaller than **MAX_LINKID_TEXT**.  
  
## Remarks  
 Retrieves the ID of a specific link control item. For more information, see the Win32 message [LM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760720) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::SetItemID](../vs140/CLinkCtrl--SetItemID.md)   
 [CLinkCtrl::GetItem](../vs140/CLinkCtrl--GetItem.md)