---
title: "CRect::OffsetRect"
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
ms.assetid: 46b73ee1-17f6-4426-a85d-dd0f521d7e1e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::OffsetRect
Moves `CRect` by the specified offsets.  
  
## Syntax  
  
```  
  
      void OffsetRect(   
   int x,   
   int y    
) throw( );  
void OffsetRect(   
   POINT point    
) throw( );  
void OffsetRect(   
   SIZE size    
) throw( );  
```  
  
#### Parameters  
 *x*  
 Specifies the amount to move left or right. It must be negative to move left.  
  
 *y*  
 Specifies the amount to move up or down. It must be negative to move up.  
  
 `point`  
 Contains a [POINT](../vs140/POINT-Structure.md) structure or [CPoint](../vs140/CPoint-Class.md) object specifying both dimensions by which to move.  
  
 `size`  
 Contains a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object specifying both dimensions by which to move.  
  
## Remarks  
 Moves `CRect` *x* units along the x-axis and *y* units along the y-axis. The *x* and *y* parameters are signed values, so `CRect` can be moved left or right and up or down.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#50](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#50)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator +](../vs140/CRect--operator--.md)   
 [CRect::operator +=](../vs140/CRect--operator--=.md)   
 [CRect::operator -](../vs140/CRect--operator--.md)   
 [CRect::operator -=](../vs140/CRect--operator--=.md)