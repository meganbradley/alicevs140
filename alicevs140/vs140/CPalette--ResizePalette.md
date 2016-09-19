---
title: "CPalette::ResizePalette"
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
ms.assetid: 3207bf3c-04df-4511-b6d8-415d0cfb1d25
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPalette::ResizePalette
Changes the size of the logical palette attached to the `CPalette` object to the number of entries specified by `nNumEntries`.  
  
## Syntax  
  
```  
  
      BOOL ResizePalette(  
   UINT nNumEntries   
);  
```  
  
#### Parameters  
 `nNumEntries`  
 Specifies the number of entries in the palette after it has been resized.  
  
## Return Value  
 Nonzero if the palette was successfully resized; otherwise 0.  
  
## Remarks  
 If an application calls `ResizePalette` to reduce the size of the palette, the entries remaining in the resized palette are unchanged. If the application calls `ResizePalette` to enlarge the palette, the additional palette entries are set to black (the red, green, and blue values are all 0), and the flags for all additional entries are set to 0.  
  
 For more information on the Windows API `ResizePalette`, see [ResizePalette](http://msdn.microsoft.com/library/windows/desktop/dd162928) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPalette Class](../vs140/CPalette-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ResizePalette](http://msdn.microsoft.com/library/windows/desktop/dd162928)