---
title: "CDataPathProperty::ResetData"
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
ms.assetid: f096a8cf-761f-4e5e-ba75-d81a47bb285f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataPathProperty::ResetData
Call this function to get `CAsyncMonikerFile::OnDataAvailable` to notify the container that the control properties have changed, and all the information loaded asynchronously is no longer useful.  
  
## Syntax  
  
```  
  
virtual void ResetData( );  
```  
  
## Remarks  
 Opening should be restarted. Derived classes can override this function for different defaults.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncMonikerFile::OnDataAvailable](../vs140/CAsyncMonikerFile--OnDataAvailable.md)   
 [CDataPathProperty::Open](../vs140/CDataPathProperty--Open.md)