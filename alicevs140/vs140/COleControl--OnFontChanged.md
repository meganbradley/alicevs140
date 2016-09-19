---
title: "COleControl::OnFontChanged"
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
ms.assetid: 91a5fda5-d04f-48fd-bb6d-f0d0cb2d732d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnFontChanged
Called by the framework when the stock Font property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnFontChanged( );  
```  
  
## Remarks  
 The default implementation calls `COleControl::InvalidateControl`. If the control is subclassing a Windows control, the default implementation also sends a **WM_SETFONT** message to the control's window.  
  
 Override this function if you want notification after this property changes.  
  
## Example  
 [!CODE [NVC_MFCAxCtl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#6)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetFont](../vs140/COleControl--GetFont.md)   
 [COleControl::InternalGetFont](../vs140/COleControl--InternalGetFont.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)