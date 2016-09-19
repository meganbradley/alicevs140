---
title: "Using an Image List"
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
ms.assetid: e0aed188-a1e6-400e-9f51-033d61c5541f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using an Image List
Typical usage of an image list follows the pattern below:  
  
-   Construct a [CImageList](../vs140/CImageList-Class.md) object and call one of the overloads of its [Create](../vs140/CImageList--Create.md) function to create an image list and attach it to the `CImageList` object.  
  
-   If you didn't add images when you created the image list, add images to the image list by calling the [Add](../vs140/CImageList--Add.md) or [Read](../vs140/CImageList--Read.md) member function.  
  
-   Associate the image list with a control by calling the appropriate member function of that control, or draw images from the image list yourself using the image list's [Draw](../vs140/CImageList--Draw.md) member function.  
  
-   Perhaps allow the user to drag an image, using the image list's built-in support for dragging.  
  
> [!NOTE]
>  If the image list was created with the **new** operator, you must destroy the `CImageList` object when you are done with it.  
  
## See Also  
 [Using CImageList](../vs140/Using-CImageList.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)