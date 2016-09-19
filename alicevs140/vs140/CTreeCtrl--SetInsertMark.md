---
title: "CTreeCtrl::SetInsertMark"
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
ms.assetid: 21356b64-20c7-4891-a742-53b29f499695
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetInsertMark
This member function implements the behavior of the Win32 message [TVM_SETINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb773753), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL SetInsertMark(  
   HTREEITEM hItem,  
   BOOL fAfter = TRUE   
);  
```  
  
#### Parameters  
 `hItem`  
 **HTREEITEM** that specifies at which item the insertion mark will be placed. If this argument is **NULL**, the insertion mark is removed.  
  
 *fAfter*  
 **BOOL** value that specifies if the insertion mark is placed before or after the specified item. If this argument is nonzero, the insertion mark will be placed after the item. If this argument is zero, the insertion mark will be placed before the item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#31)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)