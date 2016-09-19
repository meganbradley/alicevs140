---
title: "CAsyncMonikerFile::CAsyncMonikerFile"
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
ms.assetid: 03870e69-7a2e-41c9-87e1-6b8622e64826
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::CAsyncMonikerFile
Constructs a `CAsyncMonikerFile` object.  
  
## Syntax  
  
```  
  
CAsyncMonikerFile( );  
```  
  
## Remarks  
 It does not create the `IBindHost` interface. `IBindHost` is used only if you provide it in the **Open** member function.  
  
 For a description of the `IBindHost` interface, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [CAsyncMonikerFile::Open](../vs140/CAsyncMonikerFile--Open.md)