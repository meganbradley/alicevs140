---
title: "FtmBase::GetMarshalSizeMax Method"
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
ms.assetid: b416b1bf-c73e-45d5-abb8-04921c1a0c94
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FtmBase::GetMarshalSizeMax Method
Get the upper bound on the number of bytes needed to marshal the specified interface pointer on the specified object.  
  
## Syntax  
  
```  
STDMETHODIMP GetMarshalSizeMax(  
   __in REFIID riid,  
   __in_opt void *pv,  
   __in DWORD dwDestContext,  
   __reserved void *pvDestContext,  
   __in DWORD mshlflags,  
   __out DWORD *pSize  
) override;  
```  
  
#### Parameters  
 `riid`  
 Reference to the identifier of the interface to be marshaled.  
  
 `pv`  
 Interface pointer to be marshaled; can be NULL.  
  
 `dwDestContext`  
 Destination context where the specified interface is to be unmarshaled.  
  
 Specify one or more MSHCTX enumeration values.  
  
 Currently, unmarshaling can occur either in another apartment of the current process (MSHCTX_INPROC) or in another process on the same computer as the current process (MSHCTX_LOCAL).  
  
 `pvDestContext`  
 Reserved for future use; must be NULL.  
  
 `mshlflags`  
 Flag indicating whether the data to be marshaled is to be transmitted back to the client process — the typical case — or written to a global table, where it can be retrieved by multiple clients. Specify one or more MSHLFLAGS enumeration values.  
  
 `pSize`  
 When this operation completes, pointer to the upper bound on the amount of data to be written to the marshaling stream.  
  
## Return Value  
 S_OK if successful; otherwise, E_FAIL or E_NOINTERFACE.  
  
## Requirements  
 **Header:** ftm.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [FtmBase Class](../vs140/FtmBase-Class.md)