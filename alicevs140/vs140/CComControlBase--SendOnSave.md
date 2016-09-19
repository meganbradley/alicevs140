---
title: "CComControlBase::SendOnSave"
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
ms.assetid: e8768764-d8ca-4e2c-9758-963c6ddd3835
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::SendOnSave
Notifies all advisory sinks registered with the advise holder that the control has been saved.  
  
## Syntax  
  
```  
  
HRESULT SendOnSave( );  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Sends a notification that the control has just saved its data.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_spOleAdviseHolder](../vs140/CComControlBase--m_spOleAdviseHolder.md)