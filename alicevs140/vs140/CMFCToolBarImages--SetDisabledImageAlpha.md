---
title: "CMFCToolBarImages::SetDisabledImageAlpha"
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
ms.assetid: ad0936e2-a0cc-44c4-be3c-8e3fce0f298a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::SetDisabledImageAlpha
Sets the alpha channel (opacity) value that is used for disabled images.  
  
## Syntax  
  
```  
static void SetDisabledImageAlpha(  
   BYTE nValue   
);  
```  
  
#### Parameters  
 [in] `nValue`  
 The new value of the alpha channel.  
  
## Remarks  
 Use this method to set a custom alpha value for disabled images. The default value is 127, which causes disabled button images to be semitransparent. If you set a value of 0, disabled images will be completely transparent. If you set a value of 255, disabled images will be completely opaque.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)