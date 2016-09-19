---
title: "IDebugBreakpointRequest2::GetLocationType"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b6d14c59-d3aa-48ff-8278-f6b5bba9c2f3
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointRequest2::GetLocationType
Gets the breakpoint location type of this breakpoint request.  
  
## Syntax  
  
```cpp#  
HRESULT GetLocationType(   
   BP_LOCATION_TYPE* pBPLocationType  
);  
```  
  
```c#  
int GetLocationType(   
   out enum_BP_LOCATION_TYPE pBPLocationType  
);  
```  
  
#### Parameters  
 `pBPLocationType`  
 [out] Returns a value from the [BP_LOCATION_TYPE](../vs140/BP_LOCATION_TYPE.md) enumeration that describes the location of this breakpoint request.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_FAIL` if the `bpLocation` field in the associated [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) structure is not valid.  
  
## Example  
 The following example shows how to implement this method for a simple `CDebugBreakpointRequest` object that exposes the[IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md) interface.  
  
```  
HRESULT CDebugBreakpointRequest::GetLocationType(BP_LOCATION_TYPE* pBPLocationType)    
{    
   HRESULT hr;    
  
   if (pBPLocationType)    
   {    
      // Set default BP_LOCATION_TYPE.    
      *pBPLocationType = BPLT_NONE;    
  
      // Check if the BPREQI_BPLOCATION flag is set in BPREQI_FIELDS.    
      if (IsFlagSet(m_bpRequestInfo.dwFields, BPREQI_BPLOCATION))    
      {    
         // Get the new BP_LOCATION_TYPE.    
         *pBPLocationType = m_bpRequestInfo.bpLocation.bpLocationType;    
         hr = S_OK;    
      }    
      else    
      {    
         hr = E_FAIL;    
      }    
   }    
   else    
   {    
      hr = E_INVALIDARG;    
   }    
  
   return hr;    
}    
```  
  
## See Also  
 [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md)   
 [BP_LOCATION_TYPE](../vs140/BP_LOCATION_TYPE.md)   
 [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)