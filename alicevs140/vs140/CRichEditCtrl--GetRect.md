---
title: "CRichEditCtrl::GetRect"
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
ms.assetid: 0c5d02d2-1ce6-484a-ba26-a0f72f7bb1dd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetRect
Retrieves the formatting rectangle for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      void GetRect(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 [CRect](../vs140/CRect-Class.md) or pointer to a [RECT](../vs140/RECT-Structure.md) to receive the formatting rectangle of this `CRichEditCtrl` object.  
  
## Remarks  
 The formatting rectangle is the bounding rectangle for the text. This value is independent of the size of the `CRichEditCtrl` object.  
  
 For more information, see [EM_GETRECT](http://msdn.microsoft.com/library/windows/desktop/bb761596) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [LimitText](../vs140/CRichEditCtrl--LimitText.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetRect](../vs140/CRichEditCtrl--SetRect.md)