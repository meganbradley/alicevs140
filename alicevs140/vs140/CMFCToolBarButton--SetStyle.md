---
title: "CMFCToolBarButton::SetStyle"
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
ms.assetid: 5d10ec23-d12a-4aa5-9a23-28bfbc1e48e8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::SetStyle
Sets the style of the button.  
  
## Syntax  
  
```  
virtual void SetStyle(  
   UINT nStyle   
);  
```  
  
#### Parameters  
 [in] `nStyle`  
 The new style of the button.  
  
## Remarks  
 The default implementation sets the [CMFCToolBarButton::m_nStyle](../vs140/CMFCToolBarButton--m_nStyle.md) data member to `nStyle`. Override this method if you want to perform additional processing to handle the change in style. See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for a list of valid style flags.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::m_nStyle](../vs140/CMFCToolBarButton--m_nStyle.md)   
 [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md)