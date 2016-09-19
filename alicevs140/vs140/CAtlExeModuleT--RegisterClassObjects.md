---
title: "CAtlExeModuleT::RegisterClassObjects"
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
ms.assetid: 1bf8b4c2-b827-4018-bb8b-799c7954d365
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::RegisterClassObjects
Registers the class object with OLE so other applications can connect to it.  
  
## Syntax  
  
```  
  
      HRESULT RegisterClassObjects(  
   DWORD dwClsContext,  
   DWORD dwFlags   
) throw( );  
```  
  
#### Parameters  
 *dwClsContext*  
 Specifies the context in which the class object is to be run. Possible values are CLSCTX_INPROC_SERVER, CLSCTX_INPROC_HANDLER, or CLSCTX_LOCAL_SERVER.  
  
 `dwFlags`  
 Determines the connection types to the class object. Possible values are REGCLS_SINGLEUSE, REGCLS_MULTIPLEUSE, or REGCLS_MULTI_SEPARATE.  
  
## Return Value  
 Returns S_OK on success, S_FALSE if there were no classes to register, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)   
 [CLSCTX](http://msdn.microsoft.com/library/windows/desktop/ms693716)   
 [REGCLS](http://msdn.microsoft.com/library/windows/desktop/ms679697)   
 [CAtlExeModuleT::RevokeClassObjects](../vs140/CAtlExeModuleT--RevokeClassObjects.md)