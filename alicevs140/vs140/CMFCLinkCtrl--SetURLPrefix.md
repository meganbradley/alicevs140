---
title: "CMFCLinkCtrl::SetURLPrefix"
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
ms.assetid: 1105ce54-db39-465b-a2f8-80a5da30a554
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCLinkCtrl::SetURLPrefix
Sets the implicit protocol (for example, "http:") of the URL.  
  
## Syntax  
  
```  
void SetURLPrefix(  
   LPCTSTR lpszPrefix   
);  
```  
  
#### Parameters  
 [in] `lpszPrefix`  
 The prefix of the URL protocol.  
  
## Remarks  
 Use this method to set the URL prefix. The prefix is not displayed on the button's face, but you can use it to help browse to the URL's target.  
  
## Requirements  
 **Header:** afxlinkctrl.h  
  
## See Also  
 [CMFCLinkCtrl Class](../vs140/CMFCLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)