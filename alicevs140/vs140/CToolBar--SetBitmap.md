---
title: "CToolBar::SetBitmap"
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
ms.assetid: 8517e61d-d7ae-4f50-bf7c-5702aa191409
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::SetBitmap
Call this member function to set the bitmap image for the toolbar.  
  
## Syntax  
  
```  
  
      BOOL SetBitmap(  
   HBITMAP hbmImageWell   
);  
```  
  
#### Parameters  
 *hbmImageWell*  
 Handle of a bitmap image that is associated with a toolbar.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 For example, call `SetBitmap` to change the bitmapped image after the user takes an action on a document that changes the action of a button.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)