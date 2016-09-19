---
title: "CToolBar::LoadToolBar"
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
ms.assetid: fa05c955-f1bf-4d0d-bccb-955085f589c6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::LoadToolBar
Call this member function to load the toolbar specified by `lpszResourceName` or `nIDResource`.  
  
## Syntax  
  
```  
  
      BOOL LoadToolBar(  
   LPCTSTR lpszResourceName   
);  
BOOL LoadToolBar(  
   UINT nIDResource   
);  
```  
  
#### Parameters  
 `lpszResourceName`  
 Pointer to the resource name of the toolbar to be loaded.  
  
 `nIDResource`  
 Resource ID of the toolbar to be loaded.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 See [toolbar editor](../vs140/Toolbar-Editor.md) in for more information about creating a toolbar resource.  
  
## Example  
 See the example for [CToolBar::CreateEx](../vs140/CToolBar--CreateEx.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::Create](../vs140/CToolBar--Create.md)   
 [CToolBar::LoadBitmap](../vs140/CToolBar--LoadBitmap.md)   
 [CToolBar::SetButtons](../vs140/CToolBar--SetButtons.md)