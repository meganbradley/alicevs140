---
title: "CRichEditCtrl::RequestResize"
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
ms.assetid: 07d75fb8-e5c3-4708-9303-0f9856302397
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::RequestResize
Forces this `CRichEditCtrl` object to send **EN_REQUESTRESIZE** notification messages to its parent window.  
  
## Syntax  
  
```  
  
void RequestResize( );  
  
```  
  
## Remarks  
 This function is useful during [CWnd::OnSize](../vs140/CWnd--OnSize.md) processing for a bottomless `CRichEditCtrl` object.  
  
 For more information, see the [EM_REQUESTRESIZE](http://msdn.microsoft.com/library/windows/desktop/bb774220) message and the **Bottomless Rich Edit Controls** section of [About Rich Edit Controls](http://msdn.microsoft.com/library/windows/desktop/bb787873) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnSize](../vs140/CWnd--OnSize.md)   
 [CRichEditCtrl::Create](../vs140/CRichEditCtrl--Create.md)