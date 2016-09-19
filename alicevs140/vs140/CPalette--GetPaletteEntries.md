---
title: "CPalette::GetPaletteEntries"
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
ms.assetid: f53416ea-eb34-4017-a1cb-c87db2fdaa5e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPalette::GetPaletteEntries
Retrieves a range of palette entries in a logical palette.  
  
## Syntax  
  
```  
  
      UINT GetPaletteEntries(  
   UINT nStartIndex,  
   UINT nNumEntries,  
   LPPALETTEENTRY lpPaletteColors   
) const;  
```  
  
#### Parameters  
 `nStartIndex`  
 Specifies the first entry in the logical palette to be retrieved.  
  
 `nNumEntries`  
 Specifies the number of entries in the logical palette to be retrieved.  
  
 `lpPaletteColors`  
 Points to an array of [PALETTEENTRY](http://msdn.microsoft.com/library/windows/desktop/dd162769) data structures to receive the palette entries. The array must contain at least as many data structures as specified by `nNumEntries`.  
  
## Return Value  
 The number of entries retrieved from the logical palette; 0 if the function failed.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPalette Class](../vs140/CPalette-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetPaletteEntries](http://msdn.microsoft.com/library/windows/desktop/dd144907)   
 [CPalette::SetPaletteEntries](../vs140/CPalette--SetPaletteEntries.md)