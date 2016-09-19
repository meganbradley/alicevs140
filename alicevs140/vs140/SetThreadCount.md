---
title: "SetThreadCount"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SetThreadCount
apilocation: 
  - filetracker.dll
apitype: COM
ms.assetid: 335335a5-8ca0-4e18-95f5-62aa6a691386
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetThreadCount
Sets the global thread count, and assigns that count to the current thread.  
  
## Syntax  
  
```  
HRESULT WINAPI SetThreadCount(int threadCount);  
```  
  
#### Parameters  
 [in] `threadCount`  
 The number of threads to use.  
  
## Return Value  
 An [HRESULT](assetId:///HRESULT?qualifyHint=False&autoUpgrade=True) with the [SUCCEEDED](assetId:///SUCCEEDED?qualifyHint=False&autoUpgrade=True) bit set if the thread count was updated.  
  
## Requirements  
 **Header:** FileTracker.h