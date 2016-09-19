---
title: "CMFCCustomColorsPropertyPage::Setup"
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
ms.assetid: 48b4461e-e39b-4363-aa45-1eddb3903bab
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCustomColorsPropertyPage::Setup
Sets the color components of the property page.  
  
## Syntax  
  
```  
void Setup(  
   BYTE R,  
   BYTE G,  
   BYTE B  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `R`|The red component of the RGB value.|  
|[in] `G`|The green component of the RGB value.|  
|[in] `B`|The blue component of the RGB value.|  
  
## Remarks  
 This method updates the current RGB and the associated HLS (hue, lightness, and saturation) color values of the property page. The [CMFCColorDialog::SetPageTwo](../vs140/CMFCColorDialog--SetPageTwo.md) method calls this method when the framework initializes the color dialog box or the user presses the left mouse button. For more information about `CMFCColorDialog`, see [CMFCColorDialog Class](../vs140/CMFCColorDialog-Class.md).  
  
## Requirements  
 **Header:** afxcustomcolorspropertypage.h  
  
## See Also  
 [CMFCCustomColorsPropertyPage Class](../vs140/CMFCCustomColorsPropertyPage-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCColorDialog Class](../vs140/CMFCColorDialog-Class.md)   
 [CMFCColorDialog::SetPageTwo](../vs140/CMFCColorDialog--SetPageTwo.md)