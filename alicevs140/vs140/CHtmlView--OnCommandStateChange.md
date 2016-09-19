---
title: "CHtmlView::OnCommandStateChange"
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
ms.assetid: b82b65a8-7a31-4055-b9f8-549e2277ed84
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnCommandStateChange
This member function is called by the framework to notify an application that the enabled state of a web browser command has changed.  
  
## Syntax  
  
```  
  
      virtual void OnCommandStateChange(  
   long nCommand,  
   BOOL bEnable   
);  
```  
  
#### Parameters  
 *nCommand*  
 Identifier of the command whose enabled state has changed.  
  
 `bEnable`  
 Enabled state. This parameter is nonzero if the command is enabled, or zero if it is disabled.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetReadyState](../vs140/CHtmlView--GetReadyState.md)