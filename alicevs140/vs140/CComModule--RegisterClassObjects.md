---
title: "CComModule::RegisterClassObjects"
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
ms.assetid: 2203fa5a-711e-44bf-a78f-b5a039a32472
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::RegisterClassObjects
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT RegisterClassObjects(  
   DWORD dwClsContext,  
   DWORD dwFlags   
) throw( );  
```  
  
#### Parameters  
 `dwClsContext`  
 [in] Specifies the context in which the class object is to be run. Possible values are **CLSCTX_INPROC_SERVER**, **CLSCTX_INPROC_HANDLER**, or **CLSCTX_LOCAL_SERVER**. For a description of these values, see [CLSCTX](http://msdn.microsoft.com/library/windows/desktop/ms693716) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `dwFlags`  
 [in] Determines the connection types to the class object. Possible values are **REGCLS_SINGLEUSE**, **REGCLS_MULTIPLEUSE**, or **REGCLS_MULTI_SEPARATE**. For a description of these values, see [REGCLS](http://msdn.microsoft.com/library/windows/desktop/ms679697) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Registers an EXE class object with OLE so other applications can connect to it. This methodis only available to EXEs.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::RevokeClassObjects](../vs140/CComModule--RevokeClassObjects.md)