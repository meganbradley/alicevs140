---
title: "CMFCToolBarImages::PrepareDrawImage"
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
ms.assetid: 07e47392-d163-4734-a6e5-7b7f9ae8635f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::PrepareDrawImage
Allocates the resources that are required to draw a toolbar image at a specified size.  
  
## Syntax  
  
```  
BOOL PrepareDrawImage(  
   CAfxDrawState& ds,  
   CSize sizeImageDest=CSize(0,0)  
   BOOL bFadeInactive=FALSE   
);  
```  
  
#### Parameters  
 [in] `ds`  
 A reference to `CAfxDrawState` structure, which stores the allocated resources between image rendering stages.  
  
 [in] `sizeImageDest`  
 Specifies the size of a destination image.  
  
 [in] `bFadeInactive`  
 `TRUE` if you want inactive images to be drawn faded.  
  
## Return Value  
 `TRUE` if the resources required to draw the toolbar image were allocated successfully, otherwise `FALSE`.  
  
## Remarks  
 After you call this method, you can call [CMFCToolBarImages::Draw](../vs140/CMFCToolBarImages--Draw.md) any number of times. After you finished drawing, you must call [CMFCToolBarImages::EndDrawImage](../vs140/CMFCToolBarImages--EndDrawImage.md) to release the resources allocated by `PrepareDrawImage`.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)