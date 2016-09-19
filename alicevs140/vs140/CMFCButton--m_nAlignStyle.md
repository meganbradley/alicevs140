---
title: "CMFCButton::m_nAlignStyle"
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
ms.assetid: 62116afa-5f51-41a0-a60b-5645594b0b49
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::m_nAlignStyle
Specifies the alignment of the button text.  
  
## Syntax  
  
```  
AlignStyle m_nAlignStyle;  
```  
  
## Remarks  
 Use one of the following `CMFCButton::AlignStyle` enumeration values to specify the alignment of the button text:  
  
|Value|Description|  
|-----------|-----------------|  
|ALIGN_CENTER|(Default) Aligns the button text to the center of the button.|  
|ALIGN_LEFT|Aligns the button text to the left side of the button.|  
|ALIGN_RIGHT|Aligns the button text to the right side of the button.|  
  
 The `CMFCButton` constructor initializes this member to ALIGN_CENTER.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)