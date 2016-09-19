---
title: "CHeaderCtrl::GetBitmapMargin"
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
ms.assetid: 54f43387-b758-473c-9531-11b2a70982bc
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetBitmapMargin
Retrieves the width of the margin of a bitmap in a header control.  
  
## Syntax  
  
```  
  
int GetBitmapMargin( ) const;  
  
```  
  
## Return Value  
 The width of the bitmap margin in pixels.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_GETBITMAPMARGIN](http://msdn.microsoft.com/library/windows/desktop/bb775314), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#8)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::SetBitmapMargin](../vs140/CHeaderCtrl--SetBitmapMargin.md)