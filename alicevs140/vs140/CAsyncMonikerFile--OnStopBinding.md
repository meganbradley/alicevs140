---
title: "CAsyncMonikerFile::OnStopBinding"
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
ms.assetid: b760fa17-fe7b-47a7-8ed3-5ed21dd2a8dd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::OnStopBinding
Called by the moniker at the end of the bind operation.  
  
## Syntax  
  
```  
  
      virtual void OnStopBinding(  
   HRESULT hresult,  
   LPCTSTR szError   
);  
```  
  
#### Parameters  
 `hresult`  
 An `HRESULT` that is the error or warning value.  
  
 *szErrort*  
 A character string describing the error.  
  
## Remarks  
 Override this function to perform actions when the transfer is stopped. By default, the function releases `IBinding`.  
  
 For a description of the `IBinding` interface, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncMonikerFile::OnStartBinding](../vs140/CAsyncMonikerFile--OnStartBinding.md)