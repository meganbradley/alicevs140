---
title: "CHtmlEditCtrlBase::GetIsDirty"
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
ms.assetid: efc1bff9-c4a0-4580-836e-dc2d0bc6dd9d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetIsDirty
Indicates whether the HTML document has changed.  
  
## Syntax  
  
```  
  
HRESULT GetIsDirty( ) const;  
  
```  
  
## Remarks  
 Indicates whether the document has changed. `GetIsDirty` returns an `HRESULT` from [IPersistStorage::IsDirty](http://msdn.microsoft.com/library/windows/desktop/ms683910).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)