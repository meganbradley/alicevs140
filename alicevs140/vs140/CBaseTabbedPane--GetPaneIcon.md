---
title: "CBaseTabbedPane::GetPaneIcon"
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
ms.assetid: 8624d1b5-c011-4742-a718-e0a2899b63e1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::GetPaneIcon
Retrieves the minimum allowed size for the pane.  
  
## Syntax  
  
```  
virtual void GetMinSize(  
   CSize& size  
) const;  
```  
  
#### Parameters  
 [out] `size`  
 A `CSize` object that is filled with the minimum allowed size.  
  
## Remarks  
 If consistent handling of minimum pane sizes is active ([CPane::m_bHandleMinSize](../vs140/CPane--m_bHandleMinSize.md)), `size` is filled with the minimum allowed size for the active tab. Otherwise, `size` is filled with the return value of [CPane::GetMinSize](../vs140/CPane--GetMinSize.md).  
  
## Requirements  
 **Header:** afxbasetabbedpane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)