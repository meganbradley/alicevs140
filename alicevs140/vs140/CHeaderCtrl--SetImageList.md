---
title: "CHeaderCtrl::SetImageList"
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
ms.assetid: eba5917b-98c9-4f7f-900f-e0820a5e6249
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::SetImageList
Assigns an image list to a header control.  
  
## Syntax  
  
```  
  
      CImageList* SetImageList(  
   CImageList* pImageList   
);  
```  
  
#### Parameters  
 `pImageList`  
 A pointer to a `CImageList` object containing the image list to be assigned to the header control.  
  
## Return Value  
 A pointer to the [CImageList](../vs140/CImageList-Class.md) object previously assigned to the header control.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_SETIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb775365), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The `CImageList` object to which the returned pointer points is a temporary object and is deleted in the next idle-time processing.  
  
## Example  
 See the example for [CHeaderCtrl::GetImageList](../vs140/CHeaderCtrl--GetImageList.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::GetImageList](../vs140/CHeaderCtrl--GetImageList.md)   
 [CHeaderCtrl::CreateDragImage](../vs140/CHeaderCtrl--CreateDragImage.md)