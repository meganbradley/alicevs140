---
title: "CAsyncMonikerFile::GetBindInfo"
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
ms.assetid: 90252d1b-2d50-46cc-bd86-5f72e70e8f78
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::GetBindInfo
Called from the client of an asynchronous moniker to tell the asynchronous moniker how it wants to bind.  
  
## Syntax  
  
```  
  
virtual DWORD GetBindInfo( ) const;  
```  
  
## Return Value  
 Retrieves the settings for **IBindStatusCallBack**. For a description of the `IBindStatusCallback` interface, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 The default implementation sets the binding to be asynchronous, to use a storage medium (a stream), and to use the data-push model. Override this function if you want to change the behavior of the binding.  
  
 One reason for doing this would be to bind using the data-pull model instead of the data-push model. In a data-pull model, the client drives the bind operation, and the moniker only provides data to the client when it is read. In a data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)