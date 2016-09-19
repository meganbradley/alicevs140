---
title: "CMFCRibbonButtonsGroup::SetImages"
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
ms.assetid: caa0d1ac-5f63-442d-a375-c8e5879ebaef
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButtonsGroup::SetImages
Assigns images to the group of ribbon buttons.  
  
## Syntax  
  
```  
void SetImages(  
   CMFCToolBarImages* pImages,  
   CMFCToolBarImages* pHotImages,  
   CMFCToolBarImages* pDisabledImages   
);  
```  
  
#### Parameters  
 [in] `pImages`  
 Regular images.  
  
 [in] `pHotImages`  
 Hot images.  
  
 [in] `pDisabledImages`  
 Disabled images.  
  
## Remarks  
 Call `SetImages` before you add buttons to a group. The number of images must be greater or equal to the number of buttons to be added to the group.  
  
> [!NOTE]
>  Hot images are images that are displayed when the user hovers over the button. Disabled images are images that are displayed when the button is disabled.  
  
## Requirements  
 **Header:** afxribbonbuttonsgroup.h  
  
## See Also  
 [CMFCRibbonButtonsGroup Class](../vs140/CMFCRibbonButtonsGroup-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)