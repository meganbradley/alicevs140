---
title: "IDebugModule2::GetInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de337e66-294f-4ac9-b21e-71fac7418e36
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule2::GetInfo
Gets information about this module.  
  
## Syntax  
  
```cpp#  
HRESULT GetInfo(   
   MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO*       pInfo  
);  
```  
  
```cpp#  
int GetInfo(   
   enum_MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO[]           pInfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [MODULE_INFO_FIELDS](../vs140/MODULE_INFO_FIELDS.md) enumeration that specify which fields of `pInfo` are to be filled out.  
  
 `pInfo`  
 [in, out] A [MODULE_INFO](../vs140/MODULE_INFO.md) structure that is filled in with a description of the module.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The [MODULE_INFO](../vs140/MODULE_INFO.md) structure contains the name of the module that is displayed in the **Modules** window.  
  
## See Also  
 [IDebugModule2](../vs140/IDebugModule2.md)   
 [MODULE_INFO_FIELDS](../vs140/MODULE_INFO_FIELDS.md)   
 [MODULE_INFO](../vs140/MODULE_INFO.md)