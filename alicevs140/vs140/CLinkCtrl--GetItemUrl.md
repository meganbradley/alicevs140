---
title: "CLinkCtrl::GetItemUrl"
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
ms.assetid: a1dc236e-afc3-4dd3-a47e-42ad4a680318
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::GetItemUrl
Retrieves the URL represented by the link control item.  
  
## Syntax  
  
```  
  
      BOOL GetItemUrl(  
   int iLink,  
   CString& strUrl   
) const;  
BOOL GetItemUrl(  
   int iLink,  
   LPWSTR szUrl,  
   UINT cchUrl   
) const;  
```  
  
#### Parameters  
 `iLink`  
 The index of a link control item.  
  
 `strUrl`  
 A [CStringT](../vs140/CStringT-Class.md) object containing the URL represented by the specified item  
  
 `szUrl`  
 A null-terminated string containing the URL represented by the specified item  
  
 *cchUrl*  
 The size in characters of the *szURL* buffer.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
> [!NOTE]
>  This function also returns **FALSE** if the buffer of *szUrl or strUrl* is smaller than **MAX_LINKID_TEXT**.  
  
## Remarks  
 Retrieves the URL represented by the specified link control item. For more information, see the Win32 message [LM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760720) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::SetItemUrl](../vs140/CLinkCtrl--SetItemUrl.md)   
 [CLinkCtrl::GetItem](../vs140/CLinkCtrl--GetItem.md)