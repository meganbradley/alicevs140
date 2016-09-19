---
title: "FtmBase::GetUnmarshalClass Method"
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
ms.assetid: 535fc539-5b97-4967-b158-f7568f13d341
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FtmBase::GetUnmarshalClass Method
Gets the CLSID that COM uses to locate the DLL containing the code for the corresponding proxy. COM loads this DLL to create an uninitialized instance of the proxy.  
  
## Syntax  
  
```  
STDMETHODIMP GetUnmarshalClass(  
   __in REFIID riid,  
   __in_opt void *pv,  
   __in DWORD dwDestContext,  
   __reserved void *pvDestContext,  
   __in DWORD mshlflags,  
   __out CLSID *pCid  
) override;  
```  
  
#### Parameters  
 `riid`  
 Reference to the identifier of the interface to be marshaled.  
  
 `pv`  
 Pointer to the interface to be marshaled; can be NULL if the caller does not have a pointer to the desired interface.  
  
 `dwDestContext`  
 Destination context where the specified interface is to be unmarshaled.  
  
 Specify one or more MSHCTX enumeration values.  
  
 Unmarshaling can occur either in another apartment of the current process (MSHCTX_INPROC) or in another process on the same computer as the current process (MSHCTX_LOCAL).  
  
 `pvDestContext`  
 Reserved for future use; must be NULL.  
  
 `mshlflags`  
 When this operation completes, pointer to the CLSID to be used to create a proxy in the client process.  
  
 `pCid`  
  
## Return Value  
 S_OK if successful; otherwise, S_FALSE.  
  
## Requirements  
 **Header:** ftm.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [FtmBase Class](../vs140/FtmBase-Class.md)