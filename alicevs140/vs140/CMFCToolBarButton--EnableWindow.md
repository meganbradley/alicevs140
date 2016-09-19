---
title: "CMFCToolBarButton::EnableWindow"
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
ms.assetid: c59de29e-7463-484f-8b06-c256a44f7073
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::EnableWindow
Enables or disables mouse and keyboard input.  
  
## Syntax  
  
```  
virtual void EnableWindow(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 Set this parameter to `TRUE` to enable input, or to `FALSE` to disable input.  
  
## Remarks  
 This method calls the `EnableWindow` function to enable or disable input. For more information, see [EnableWindow](http://msdn.microsoft.com/library/windows/desktop/ms646291) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [EnableWindow](http://msdn.microsoft.com/library/windows/desktop/ms646291)