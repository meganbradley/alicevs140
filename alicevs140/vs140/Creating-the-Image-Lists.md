---
title: "Creating the Image Lists"
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
ms.assetid: c2768515-deba-49e8-a6f3-5be6482afb19
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating the Image Lists
Creating image lists is the same whether you use [CListView](../vs140/CListView-Class.md) or [CListCtrl](../vs140/CListCtrl-Class.md).  
  
> [!NOTE]
>  You only need image lists if your list control includes the `LVS_ICON` style.  
  
 Use class `CImageList` to create one or more image lists (for full-size icons, small icons, and states). See [CImageList](../vs140/CImageList-Class.md), and see [List View Image Lists](http://msdn.microsoft.com/library/windows/desktop/bb774736) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Call [CListCtrl::SetImageList](../vs140/CListCtrl--SetImageList.md) for each image list; pass a pointer to the appropriate `CImageList` object.  
  
## See Also  
 [Using CListCtrl](../vs140/Using-CListCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)