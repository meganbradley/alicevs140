---
title: "CMFCDynamicLayout::MoveSettings Structure"
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
ms.assetid: 48a9bd38-5067-4407-8751-eafb01b150a8
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::MoveSettings Structure
Encapsulates move data for controls in a dynamic layout.  
  
## Syntax  
  
```  
struct CMFCDynamicLayout::MoveSettings;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`MoveSettings`|Constructs the object with zero default values.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[MoveSettings::IsHorizontal](../vs140/MoveSettings--IsHorizontal.md)|Checks if the move data specifies a nonzero horizontal movement.|  
|[MoveSettings::IsNone](../vs140/MoveSettings--IsNone.md)|Checks if the move data specifies no movement.|  
|[MoveSettings::IsVertical](../vs140/MoveSettings--IsVertical.md)|Checks if the move data specifies a nonzero vertical movement.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|`m_nXRatio`|The amount to move horizontally, as a percentage.|  
|`m_nYRatio`|The amount to move vertically, as a percentage.|  
  
## Remarks  
 This is a nested class inside `CMFCDynamicLayout`.  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::SizeSettings](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md)