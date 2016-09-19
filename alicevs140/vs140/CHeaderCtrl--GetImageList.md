---
title: "CHeaderCtrl::GetImageList"
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
ms.assetid: 0b523368-ab46-4aaf-9f31-e40922b53be8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetImageList
Retrieves the handle of an image list used for drawing header items in a header control.  
  
## Syntax  
  
```  
  
CImageList* GetImageList( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_GETIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb775332), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The `CImageList` object to which the returned pointer points is a temporary object and is deleted in the next idle-time processing.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::SetImageList](../vs140/CHeaderCtrl--SetImageList.md)   
 [CHeaderCtrl::CreateDragImage](../vs140/CHeaderCtrl--CreateDragImage.md)