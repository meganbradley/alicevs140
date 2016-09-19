---
title: "Tree Control Image Lists"
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
ms.assetid: f560c4f2-20d2-4d28-ac33-4017e65fb0a6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tree Control Image Lists
Each item in a tree control ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)) can have a pair of bitmapped images associated with it. The images appear on the left side of an item's label. One image is displayed when the item is selected, and the other is displayed when the item is not selected. For example, an item might display an open folder when it is selected and a closed folder when it is not selected.  
  
 To use item images, you must create an image list by constructing a [CImageList](../vs140/CImageList-Class.md) object and using the [CImageList::Create](../vs140/CImageList--Create.md) function to create the associated image list. Then add the desired bitmaps to the list, and associate the list with the tree control by using the [SetImageList](../vs140/CTreeCtrl--SetImageList.md) member function. By default, all items display the first image in the image list for both the selected and nonselected states. You can change the default behavior for a particular item by specifying the indexes of the selected and nonselected images when adding the item to the tree control using the [InsertItem](../vs140/CTreeCtrl--InsertItem.md) member function. You can change the indexes after adding an item by using the [SetItemImage](../vs140/CTreeCtrl--SetItemImage.md) member function.  
  
 A tree control's image lists can also contain overlay images, which are designed to be superimposed on item images. A nonzero value in bits 8 through 11 of a tree control item's state specifies the one-based index of an overlay image (0 indicates no overlay image). Because a 4-bit, one-based index is used, overlay images must be among the first 15 images in the image lists. For more information about tree control item states, see [Tree Control Item States Overview](../vs140/Tree-Control-Item-States-Overview.md) earlier in this topic.  
  
 If a state image list is specified, a tree control reserves space to the left of each item's icon for a state image. An application can use state images, such as checked and cleared check boxes, to indicate application-defined item states. A nonzero value in bits 12 through 15 specifies the one-based index of a state image (0 indicates no state image).  
  
 By specifying the **I_IMAGECALLBACK** value instead of the index of an image, you can delay specifying the selected or nonselected image until the item is about to be redrawn. **I_IMAGECALLBACK** directs the tree control to query the application for the index by sending the [TVN_GETDISPINFO](http://msdn.microsoft.com/library/windows/desktop/bb773518) notification message.  
  
 The [GetImageList](../vs140/CTreeCtrl--GetImageList.md) member function retrieves the handle of a tree control's image list. This function is useful if you need to add more images to the list. For more information about image lists, see [Using CImageList](../vs140/Using-CImageList.md), [CImageList](../vs140/CImageList-Class.md) in the *MFC Reference*, and [Image Lists](http://msdn.microsoft.com/library/windows/desktop/bb761389) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Using CTreeCtrl](../vs140/Using-CTreeCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)