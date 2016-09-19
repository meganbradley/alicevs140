---
title: "CWndClassInfo::Register"
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
ms.assetid: bc31a034-c6ef-4dd9-8fa4-c68b72bbe08c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::Register
Called by [CWindowImpl::Create](../vs140/CWindowImpl--Create.md) to register the window class if it has not yet been registered.  
  
## Syntax  
  
```  
  
      ATOM Register(  
   WNDPROC* pProc   
);  
```  
  
#### Parameters  
 `pProc`  
 [out] Specifies the original window procedure of an existing window class.  
  
## Return Value  
 If successful, an atom that uniquely identifies the window class being registered. Otherwise, 0.  
  
## Remarks  
 If you have specified the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) (the default in [CWindowImpl](../vs140/CWindowImpl-Class.md)) or the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) macro, `Register` registers a new window class. In this case, the `pProc` parameter is not used.  
  
 If you have specified the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro, `Register` registers a superclass — a window class that is based on an existing class but uses a different window procedure. The existing window class's window procedure is returned in `pProc`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)   
 [CWndClassInfo::m_atom](../vs140/CWndClassInfo--m_atom.md)   
 [CWndClassInfo::m_wc](../vs140/CWndClassInfo--m_wc.md)   
 [CWndClassInfo::pWndProc](../vs140/CWndClassInfo--pWndProc.md)