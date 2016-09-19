---
title: "CRgn::CRgn"
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
ms.assetid: 1f28a982-51b7-43db-8ec5-116c67c95ef3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CRgn
Constructs a `CRgn` object.  
  
## Syntax  
  
```  
  
CRgn( );  
```  
  
## Remarks  
 The `m_hObject` data member does not contain a valid Windows GDI region until the object is initialized with one or more of the other `CRgn` member functions.  
  
## Example  
 See the example for [CRgn::CreateRoundRectRgn](../vs140/CRgn--CreateRoundRectRgn.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)