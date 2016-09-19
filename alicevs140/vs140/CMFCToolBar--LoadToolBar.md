---
title: "CMFCToolBar::LoadToolBar"
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
ms.assetid: 44a42479-f6eb-4397-8369-42c2cd5c95f9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::LoadToolBar
Loads the toolbar from application resources.  
  
## Syntax  
  
```  
virtual BOOL LoadToolBar(  
   UINT uiResID,  
   UINT uiColdResID=0,  
   UINT uiMenuResID=0,  
   BOOL bLocked=FALSE,  
   UINT uiDisabledResID=0,  
   UINT uiMenuDisabledResID=0,  
   UINT uiHotResID=0   
);  
```  
  
#### Parameters  
 [in] `uiResID`  
 The resource ID of the toolbar.  
  
 [in] `uiColdResID`  
 The resource ID of the bitmap that refers to the cold toolbar images.  
  
 [in] `uiMenuResID`  
 The resource ID of the bitmap that refers to the regular menu images.  
  
 [in] `bLocked`  
 A Boolean value that specifies whether the toolbar is locked or not. If this parameter is `TRUE`, the toolbar is locked. Otherwise, the toolbar is not locked.  
  
 [in] `uiDisabledResID`  
 The resource ID of the bitmap that refers to the disabled toolbar images.  
  
 [in] `uiMenuDisabledResID`  
 The resource ID of the bitmap that refers to the disabled menu images.  
  
 [in] `uiHotResID`  
 The resource ID of the bitmap that refers to the hot toolbar images.  
  
## Return Value  
 Nonzero if the method succeeds; otherwise 0.  
  
## Remarks  
 The framework calls this method during initialization to load the images that are associated with the toolbar.  
  
## Example  
 The following example demonstrates how to use the `LoadToolBar` method in the `CMFCToolBar` class. This code snippet is part of the [IE Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_IEDemo#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#6)]  
[!CODE [NVC_MFC_IEDemo#7](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#7)]  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)