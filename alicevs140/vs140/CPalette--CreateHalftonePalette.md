---
title: "CPalette::CreateHalftonePalette"
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
ms.assetid: a90873a1-d973-4e28-a438-eaf4485bd161
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPalette::CreateHalftonePalette
Creates a halftone palette for the device context.  
  
## Syntax  
  
```  
  
      BOOL CreateHalftonePalette(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 Identifies the device context.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 An application should create a halftone palette when the stretching mode of a device context is set to **HALFTONE**. The logical halftone palette returned by the [CreateHalftonePalette](http://msdn.microsoft.com/library/windows/desktop/dd183503) member function should then be selected and realized into the device context before the [CDC::StretchBlt](../vs140/CDC--StretchBlt.md) or [StretchDIBits](http://msdn.microsoft.com/library/windows/desktop/dd145121) function is called.  
  
 See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about `CreateHalftonePalette` and **StretchDIBits**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPalette Class](../vs140/CPalette-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::RealizePalette](../vs140/CDC--RealizePalette.md)   
 [CDC::SelectPalette](../vs140/CDC--SelectPalette.md)   
 [CDC::SetStretchBltMode](../vs140/CDC--SetStretchBltMode.md)   
 [CreateHalftonePalette](http://msdn.microsoft.com/library/windows/desktop/dd183503)   
 [StretchDIBits](http://msdn.microsoft.com/library/windows/desktop/dd145121)