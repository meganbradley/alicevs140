---
title: "CPalette::CreatePalette"
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
ms.assetid: 5831d9e6-970d-43b6-91f1-1ab2bd3553c4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPalette::CreatePalette
Initializes a `CPalette` object by creating a Windows logical color palette and attaching it to the `CPalette` object.  
  
## Syntax  
  
```  
  
      BOOL CreatePalette(  
   LPLOGPALETTE lpLogPalette   
);  
```  
  
#### Parameters  
 `lpLogPalette`  
 Points to a [LOGPALETTE](http://msdn.microsoft.com/library/windows/desktop/dd145040) structure that contains information about the colors in the logical palette.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about the **LOGPALETTE** structure.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPalette Class](../vs140/CPalette-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CreatePalette](http://msdn.microsoft.com/library/windows/desktop/dd183507)   
 [LOGPALETTE](http://msdn.microsoft.com/library/windows/desktop/dd145040)