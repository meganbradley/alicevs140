---
title: "IDebugBreakpointRequest3::GetRequestInfo2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33942e4a-0a0a-49e8-a693-004954f6d38a
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointRequest3::GetRequestInfo2
This method gets the breakpoint request information that describes this breakpoint request.  
  
## Syntax  
  
```cpp#  
HRESULT GetRequestInfo2(  
   BPREQI_FIELDS      dwFields,  
   BP_REQUEST_INFO2*  bBPRequestInfo  
);  
```  
  
```c#  
int GetRequestInfo2(  
   enum_BPREQI_FIELDS  dwFields,   
   BP_REQUEST_INFO2[]  bBPRequestInfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md) enumeration that determine which fields of `pBPRequestInfo` are to be filled in.  
  
 `bBPRequestInfo`  
 [out] The [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md) structure to be filled in.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## Remarks  
 There is more information in this request than is returned from the [IDebugBreakpointRequest2::GetRequestInfo](../vs140/IDebugBreakpointRequest2--GetRequestInfo.md) method.  
  
## See Also  
 [IDebugBreakpointRequest3](../vs140/IDebugBreakpointRequest3.md)   
 [IDebugBreakpointRequest2::GetRequestInfo](../vs140/IDebugBreakpointRequest2--GetRequestInfo.md)   
 [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md)   
 [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md)