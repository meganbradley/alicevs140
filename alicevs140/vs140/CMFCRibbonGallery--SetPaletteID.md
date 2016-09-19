---
title: "CMFCRibbonGallery::SetPaletteID"
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
ms.assetid: 5fd67065-2a05-4b41-9e7f-e7c44c91b460
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::SetPaletteID
Defines the command ID that is sent in the **WM_COMMAND** message when a user selects a gallery item.  
  
## Syntax  
  
```  
void SetPaletteID(  
    UINT nID   
);  
```  
  
#### Parameters  
 [in] `nID`  
 Specifies the command ID that is sent in the **WM_COMMAND** message when a user selects a gallery item.  
  
## Remarks  
 To determine the specific item that a user selected from the gallery, call the [CMFCRibbonGallery::GetLastSelectedItem](../vs140/CMFCRibbonGallery--GetLastSelectedItem.md) static method.  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)