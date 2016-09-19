---
title: "AsyncBase::CheckValidStateForResultsCall Method"
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
ms.assetid: 87ca6805-bff1-4063-b855-6dd26132deff
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBase::CheckValidStateForResultsCall Method
Tests whether the results of an asynchronous operation can be collected in the current asynchronous state.  
  
## Syntax  
  
```  
inline HRESULT CheckValidStateForResultsCall();  
```  
  
## Return Value  
 S_OK if results can be collected; otherwise, E_ILLEGAL_METHOD_CALLE_ILLEGAL_METHOD_CALL.  
  
## Requirements  
 **Header:** async.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [AsyncBase Class](../vs140/AsyncBase-Class.md)