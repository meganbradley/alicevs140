---
title: "IDebugBoundBreakpoint2::GetBreakpointResolution"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4479ac61-18a9-4a30-b213-9921c5af9a26
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBoundBreakpoint2::GetBreakpointResolution
Gets the breakpoint resolution that describes this breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT GetBreakpointResolution(   
   IDebugBreakpointResolution2** ppBPResolution  
);  
```  
  
```c#  
int GetBreakpointResolution(   
   out IDebugBreakpointResolution2 ppBPResolution  
);  
```  
  
#### Parameters  
 `ppBPResolution`  
 [out] Returns the [IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md) interface that represents one of the following:  
  
-   The breakpoint resolution object that describes the location in code where a code breakpoint has been bound.  
  
-   The data location where a data breakpoint has bound.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_BP_DELETED` if the state of the bound breakpoint object is set to `BPS_DELETED` (part of the [BP_STATE](../vs140/BP_STATE.md) enumeration).  
  
## Remarks  
 Call the [IDebugBreakpointResolution2::GetBreakpointType](../vs140/IDebugBreakpointResolution2--GetBreakpointType.md) method to determine if the breakpoint resolution is for code or data.  
  
## Example  
 The following example shows how to implement this method for a simple `CBoundBreakpoint` object that exposes the [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md) interface.  
  
```  
HRESULT CBoundBreakpoint::GetBreakpointResolution(  
    IDebugBreakpointResolution2** ppBPResolution)  
{    
   HRESULT hr;    
  
   if (ppBPResolution)    
   {    
      // Verify that the bound breakpoint has not been deleted. If   
      // deleted, then return hr = E_BP_DELETED.    
      if (m_state != BPS_DELETED)    
      {    
         // Query for the IDebugBreakpointResolution2 interface.    
         hr = m_pBPRes->QueryInterface(IID_IDebugBreakpointResolution2,  
                                       (void **)ppBPResolution);  
         assert(hr == S_OK);    
      }    
      else    
      {    
         hr = E_BP_DELETED;    
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
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md)   
 [IDebugBreakpointResolution2::GetBreakpointType](../vs140/IDebugBreakpointResolution2--GetBreakpointType.md)