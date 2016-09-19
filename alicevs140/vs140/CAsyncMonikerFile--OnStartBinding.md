---
title: "CAsyncMonikerFile::OnStartBinding"
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
ms.assetid: 85f72ecf-988b-4acb-882e-a2ed12a23e39
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::OnStartBinding
Override this function in your derived classes to perform actions when binding is starting up.  
  
## Syntax  
  
```  
  
virtual void OnStartBinding( );  
```  
  
## Remarks  
 This function is called back by the moniker. The default implementation does nothing.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncMonikerFile::OnStopBinding](../vs140/CAsyncMonikerFile--OnStopBinding.md)