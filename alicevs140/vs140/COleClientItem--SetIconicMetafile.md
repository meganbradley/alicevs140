---
title: "COleClientItem::SetIconicMetafile"
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
ms.assetid: 1ea01dac-07eb-48f6-a6b8-985299d18d11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::SetIconicMetafile
Caches the metafile used for drawing the item's icon.  
  
## Syntax  
  
```  
  
      BOOL SetIconicMetafile(  
   HGLOBAL hMetaPict   
);  
```  
  
#### Parameters  
 `hMetaPict`  
 A handle to the metafile used for drawing the item's icon.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Use [GetIconicMetafile](../vs140/COleClientItem--GetIconicMetafile.md) to retrieve the metafile.  
  
 The `hMetaPict` parameter is copied into the item; therefore, `hMetaPict` must be freed by the caller.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetIconicMetafile](../vs140/COleClientItem--GetIconicMetafile.md)