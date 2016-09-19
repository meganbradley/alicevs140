---
title: "CWnd::OnSizing"
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
ms.assetid: 71d5e3f6-dd82-437f-a319-71c377cfb632
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnSizing
The framework calls this member function to indicate that the user is resizing the rectangle.  
  
## Syntax  
  
```  
  
      afx_msg void OnSizing(  
   UINT nSide,  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `nSide`  
 The edge of window to be moved.  
  
 `lpRect`  
 Address of the [CRect](../vs140/CRect-Class.md) or [RECT](../vs140/RECT-Structure.md) structure that will contain the item's coordinates.  
  
## Remarks  
 By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#110](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#110)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)