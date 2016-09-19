---
title: "CMFCDynamicLayout::SizeSettings Structure"
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
ms.assetid: a5ce1a7a-6802-49d7-90f9-7fc6046e5f1d
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::SizeSettings Structure
Encapsulates size change data for controls in a dynamic layout.  
  
## Syntax  
  
```  
struct CMFCDynamicLayout::SizeSettings;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`SizeSettings`|Constructs the object with zero default values.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SizeSettings::IsHorizontal](../vs140/SizeSettings--IsHorizontal.md)|Checks if the resize data specifies a nonzero horizontal resizing.|  
|[SizeSettings::IsNone](../vs140/SizeSettings--IsNone.md)|Checks if the resize data specifies no resizing.|  
|[SizeSettings::IsVertical](../vs140/SizeSettings--IsVertical.md)|Checks if the resize data specifies a nonzero vertical resizing.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|`m_nXRatio`|The amount to resize horizontally, as a percentage.|  
|`m_nYRatio`|The amount to resize vertically, as a percentage.|  
  
## Remarks  
 This is a nested class inside `CMFCDynamicLayout`.  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::MoveSettings Structure](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md)