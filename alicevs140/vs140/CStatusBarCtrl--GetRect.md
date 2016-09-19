---
title: "CStatusBarCtrl::GetRect"
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
ms.assetid: 59e19c5b-6b51-4529-92da-5518ebb9719e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::GetRect
Retrieves the bounding rectangle of a part in a status bar control.  
  
## Syntax  
  
```  
  
      BOOL GetRect(  
   int nPane,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nPane`  
 Zero-based index of the part whose bounding rectangle is to be retrieved.  
  
 `lpRect`  
 Address of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#4)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetParts](../vs140/CStatusBarCtrl--GetParts.md)