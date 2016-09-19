---
title: "CPalette::AnimatePalette"
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
ms.assetid: 47fd4660-9144-4ce8-ac9f-91cb45c4a822
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPalette::AnimatePalette
Replaces entries in the logical palette attached to the `CPalette` object.  
  
## Syntax  
  
```  
  
      void AnimatePalette(  
   UINT nStartIndex,  
   UINT nNumEntries,  
   LPPALETTEENTRY lpPaletteColors   
);  
```  
  
#### Parameters  
 `nStartIndex`  
 Specifies the first entry in the palette to be animated.  
  
 `nNumEntries`  
 Specifies the number of entries in the palette to be animated.  
  
 `lpPaletteColors`  
 Points to the first member of an array of [PALETTEENTRY](http://msdn.microsoft.com/library/windows/desktop/dd162769) structures to replace the palette entries identified by `nStartIndex` and `nNumEntries`.  
  
## Remarks  
 When an application calls `AnimatePalette`, it does not have to update its client area, because Windows maps the new entries into the system palette immediately.  
  
 The `AnimatePalette` function will only change entries with the **PC_RESERVED** flag set in the corresponding **palPaletteEntry** member of the [LOGPALETTE](http://msdn.microsoft.com/library/windows/desktop/dd145040) structure that is attached to the `CPalette` object. See **LOGPALETTE** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about this structure.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPalette Class](../vs140/CPalette-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPalette::CreatePalette](../vs140/CPalette--CreatePalette.md)   
 [AnimatePalette](http://msdn.microsoft.com/library/windows/desktop/dd183355)