---
title: "CListCtrl::InsertItem"
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
ms.assetid: 1c43f981-6be7-4533-a2d9-92aa73a03ef0
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::InsertItem
Inserts an item into the list view control.  
  
## Syntax  
  
```  
int InsertItem(  
   const LVITEM* pItem   
);  
int InsertItem(  
   int nItem,  
   LPCTSTR lpszItem   
);  
int InsertItem(  
   int nItem,  
   LPCTSTR lpszItem,  
   int nImage   
);  
int InsertItem(  
   UINT nMask,  
   int nItem,  
   LPCTSTR lpszItem,  
   UINT nState,  
   UINT nStateMask,  
   int nImage,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 `pItem`  
 Pointer to an [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure that specifies the item's attributes, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `nItem`  
 Index of the item to be inserted.  
  
 `lpszItem`  
 Address of a string containing the item's label, or `LPSTR_TEXTCALLBACK` if the item is a callback item. For information on callback items, see [CListCtrl::GetCallbackMask](../vs140/CListCtrl--GetCallbackMask.md).  
  
 `nImage`  
 Index of the item's image, or `I_IMAGECALLBACK` if the item is a callback item. For information on callback items, see [CListCtrl::GetCallbackMask](../vs140/CListCtrl--GetCallbackMask.md).  
  
 `nMask`  
 The `nMask` parameter specifies which item attributes passed as parameters are valid. It can be one or more of the mask values described in [LVITEM Structure](http://msdn.microsoft.com/library/windows/desktop/bb774760) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The valid values can be combined with the bitwise OR operator.  
  
 `nState`  
 Indicates the item's state, state image, and overlay image. See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] topics [LVITEM Structure](http://msdn.microsoft.com/library/windows/desktop/bb774760) for more information and [List-View Item States](http://msdn.microsoft.com/library/windows/desktop/bb774733) for a list of valid flags.  
  
 `nStateMask`  
 Indicates which bits of the state member will be retrieved or modified. See [LVITEM Structure](http://msdn.microsoft.com/library/windows/desktop/bb774760) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
 `lParam`  
 A 32-bit application-specific value associated with the item. If this parameter is specified, you must set the `nMask` attribute `LVIF_PARAM`.  
  
## Return Value  
 The index of the new item if successful or -1 otherwise.  
  
## Remarks  
 Calling this method may cause the **LVM_INSERTITEM** message to be sent to your control window. The associated message handler for the control may fail to set the item text under certain conditions (such as using window styles such as **LVS_OWNERDRAW**). For more information on these conditions, refer to [LVM_INSERTITEM](http://msdn.microsoft.com/library/windows/desktop/bb761107) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#42](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#42)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::DeleteItem](../vs140/CListCtrl--DeleteItem.md)   
 [CListCtrl::DeleteAllItems](../vs140/CListCtrl--DeleteAllItems.md)   
 [LVM_INSERTITEM](http://msdn.microsoft.com/library/windows/desktop/bb761107)