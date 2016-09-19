---
title: "List Items and Image Lists"
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
ms.topic: article
ms.assetid: 317d095f-f978-47da-acb6-7bfe7dd3bc69
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List Items and Image Lists
An "item" in a list control ([CListCtrl](../vs140/CListCtrl-Class.md)) consists of an icon, a label, and possibly other information (in "subitems").  
  
 The icons for list control items are contained in image lists. One image list contains full-sized icons used in icon view. A second, optional, image list contains smaller versions of the same icons for use in other views of the control. A third optional list contains "state" images, such as check boxes, for display in front of the small icons in certain views. A fourth optional list contains images that are displayed in individual header items of the list control.  
  
> [!NOTE]
>  If a list view control is created with the `LVS_SHAREIMAGELISTS` style, you are responsible for destroying the image lists when they are no longer in use. Specify this style if you assign the same image lists to multiple list view controls; otherwise, more than one control might try to destroy the same image list.  
  
 For more information about list items, see [List View Image Lists](http://msdn.microsoft.com/library/windows/desktop/bb774736) and [Items and Subitems](http://msdn.microsoft.com/library/windows/desktop/bb774736) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Also see class [CImageList](../vs140/CImageList-Class.md) in the *MFC Reference* and [Using CImageList](../vs140/Using-CImageList.md) in this family of articles.  
  
 To create a list control, you need to supply image lists to be used when you insert new items into the list. The following example demonstrates this procedure, where `m_pImagelist` is a pointer of type `CImageList` and `m_listctrl` is a `CListCtrl` data member.  
  
 [!CODE [NVC_MFCControlLadenDialog#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#19)]  
  
 However, if you don't plan to display icons in your list view or list control, you don't need image lists.  
  
## See Also  
 [Using CListCtrl](../vs140/Using-CListCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)