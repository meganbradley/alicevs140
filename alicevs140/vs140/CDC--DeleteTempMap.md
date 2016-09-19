---
title: "CDC::DeleteTempMap"
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
ms.assetid: bcca71c0-8444-4c40-bb79-ff079ecf5498
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DeleteTempMap
Called automatically by the `CWinApp` idle-time handler, `DeleteTempMap` deletes any temporary `CDC` objects created by `FromHandle`, but does not destroy the device context handles (`hDC`s) temporarily associated with the `CDC` objects.  
  
## Syntax  
  
```  
  
static void PASCAL DeleteTempMap( );  
```  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Detach](../vs140/CDC--Detach.md)   
 [CDC::FromHandle](../vs140/CDC--FromHandle.md)   
 [CWinApp::OnIdle](../vs140/CWinApp--OnIdle.md)