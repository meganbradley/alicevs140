---
title: "CReBarCtrl::GetImageList"
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
ms.assetid: 78bf95e3-03f2-4865-bd38-df9a33c70018
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetImageList
Gets the `CImageList` object associated with a rebar control.  
  
## Syntax  
  
```  
  
CImageList* GetImageList( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object. Returns **NULL** if no image list is set for the control.  
  
## Remarks  
 This member function uses size and mask information stored in the [REBARINFO](http://msdn.microsoft.com/library/windows/desktop/bb774395) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::SetImageList](../vs140/CReBarCtrl--SetImageList.md)