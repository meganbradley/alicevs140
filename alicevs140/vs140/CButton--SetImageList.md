---
title: "CButton::SetImageList"
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
ms.assetid: f1ffa933-9d43-4787-98f7-6607fda01955
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetImageList
Call this method to set the image list of the `CButton` object.  
  
## Syntax  
  
```  
  
      BOOL SetImageList(  
   PBUTTON_IMAGELIST pbuttonImagelist  
);  
```  
  
#### Parameters  
 `pbuttonImagelist`  
 A pointer to the new image list.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the **BCM_SETIMAGELIST** message, as described in the [Buttons](http://msdn.microsoft.com/library/windows/desktop/bb775943) section of the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [CButton::GetImageList](../vs140/CButton--GetImageList.md)