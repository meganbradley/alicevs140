---
title: "CConnectionPoint::GetIID"
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
ms.assetid: 1f1eabad-18c5-4b45-ad5f-3b5704c38179
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CConnectionPoint::GetIID
Called by the framework to retrieve the interface ID of a connection point.  
  
## Syntax  
  
```  
  
virtual REFIID GetIID( ) = 0;  
```  
  
## Return Value  
 A reference to the connection point's interface ID.  
  
## Remarks  
 Override this function to return the interface ID for this connection point.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [CConnectionPoint Class](../vs140/CConnectionPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CONNECTION_IID](../vs140/CONNECTION_IID.md)