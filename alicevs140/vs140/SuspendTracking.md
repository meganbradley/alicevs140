---
title: "SuspendTracking"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SuspendTracking
apilocation: 
  - filetracker.dll
apitype: COM
ms.assetid: f5e06e5a-8083-444c-99c1-07ba834226b5
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SuspendTracking
Suspends tracking in the current context.  
  
## Syntax  
  
```  
HRESULT WINAPI SuspendTracking(void);  
```  
  
## Return Value  
 An [HRESULT](assetId:///HRESULT?qualifyHint=False&autoUpgrade=True) with the [SUCCEEDED](assetId:///SUCCEEDED?qualifyHint=False&autoUpgrade=True) bit set if tracking was suspended.  
  
## Requirements  
 **Header:** FileTracker.h  
  
## See Also  
 [ResumeTracking](../vs140/ResumeTracking.md)