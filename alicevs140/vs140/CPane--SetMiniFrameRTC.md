---
title: "CPane::SetMiniFrameRTC"
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
ms.assetid: bff1239f-8035-4c61-9dc8-04079fe8f53c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetMiniFrameRTC
Sets the runtime class information for the default mini-frame window.  
  
## Syntax  
  
```  
void SetMiniFrameRTC(  
    CRuntimeClass* pClass  
);  
```  
  
#### Parameters  
 [in] [out] `pClass`  
 Specifies the runtime class information for the mini-frame window.  
  
## Remarks  
 When a pane is floated, it is put on a [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md) (mini-frame) window. You can provide a custom `CPaneFrameWnd`-derived class that will be used when [CPane::CreateDefaultMiniframe](../vs140/CPane--CreateDefaultMiniframe.md) is called.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)