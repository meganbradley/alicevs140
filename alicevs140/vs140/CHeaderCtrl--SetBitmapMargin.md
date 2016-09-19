---
title: "CHeaderCtrl::SetBitmapMargin"
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
ms.assetid: 968f89fa-20f7-4f99-8219-e28de95629ee
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::SetBitmapMargin
Sets the width of the margin of a bitmap in a header control.  
  
## Syntax  
  
```  
  
      int SetBitmapMargin(  
   int nWidth   
);  
```  
  
#### Parameters  
 `nWidth`  
 Width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.  
  
## Return Value  
 The width of the bitmap margin in pixels.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_SETBITMAPMARGIN](http://msdn.microsoft.com/library/windows/desktop/bb775357), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#14)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::GetBitmapMargin](../vs140/CHeaderCtrl--GetBitmapMargin.md)