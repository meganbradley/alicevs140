---
title: "COleClientItem::GetIconicMetafile"
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
ms.assetid: f18a4b3c-8c45-42d6-abd3-ca43a2cebf19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetIconicMetafile
Retrieves the metafile used for drawing the item's icon.  
  
## Syntax  
  
```  
  
HGLOBAL GetIconicMetafile( );  
```  
  
## Return Value  
 A handle to the metafile if successful; otherwise **NULL**.  
  
## Remarks  
 If there is no current icon, a default icon is returned. This is called automatically by the MFC/OLE dialogs and is usually not called directly.  
  
 This function also calls [SetIconicMetafile](../vs140/COleClientItem--SetIconicMetafile.md) to cache the metafile for later use.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::SetIconicMetafile](../vs140/COleClientItem--SetIconicMetafile.md)