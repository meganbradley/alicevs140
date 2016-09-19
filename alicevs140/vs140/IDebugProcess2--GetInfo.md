---
title: "IDebugProcess2::GetInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46021dce-bb97-46c3-b0cc-e5b3b68acc35
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::GetInfo
Gets a description of the process.  
  
## Syntax  
  
```cpp#  
HRESULT GetInfo(  
   PROCESS_INFO_FIELDS  Fields,  
   PROCESS_INFO*        pProcessInfo  
);  
```  
  
```c#  
int GetInfo(  
   enum_PROCESS_INFO_FIELDS  Fields,  
   PROCESS_INFO[]            pProcessInfo  
);  
```  
  
#### Parameters  
 `Fields`  
 [in] A combination of values from the [PROCESS_INFO_FIELDS](../vs140/PROCESS_INFO_FIELDS.md) enumeration that specifies which fields of the `pProcessInfo` parameter are to be filled in.  
  
 `pProcessInfo`  
 [out] A [PROCESS_INFO](../vs140/PROCESS_INFO.md) structure that is filled in with a description of the process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [PROCESS_INFO_FIELDS](../vs140/PROCESS_INFO_FIELDS.md)   
 [PROCESS_INFO](../vs140/PROCESS_INFO.md)