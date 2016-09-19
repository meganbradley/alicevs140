---
title: "IDebugBreakpointBoundEvent2::EnumBoundBreakpoints"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1f588feb-522e-488d-be92-7bc19b9e3688
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointBoundEvent2::EnumBoundBreakpoints
Creates an enumerator of breakpoints that were bound on this event.  
  
## Syntax  
  
```cpp#  
HRESULT EnumBoundBreakpoints(   
   IEnumDebugBoundBreakpoints2** ppEnum  
);  
```  
  
```c#  
int EnumBoundBreakpoints(   
   out IEnumDebugBoundBreakpoints2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugBoundBreakpoints2](../vs140/IEnumDebugBoundBreakpoints2.md) object that enumerates all the breakpoints bound from this event.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no bound breakpoints; otherwise, returns an error code.  
  
## Remarks  
 The list of bound breakpoints is for those bound to this event and might not be the entire list of breakpoints bound from a pending breakpoint. To get a list of all breakpoints bound to a pending breakpoint, call the [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md) method to get the associated [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) object and then call the [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md) method to get an [IEnumDebugBoundBreakpoints2](../vs140/IEnumDebugBoundBreakpoints2.md) object which contains all the bound breakpoints for the pending breakpoint.  
  
## Example  
 The following example shows how to implement this method for a **CBreakpointSetDebugEventBase** object that exposes the [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) interface.  
  
```cpp#  
STDMETHODIMP CBreakpointSetDebugEventBase::EnumBoundBreakpoints(  
    IEnumDebugBoundBreakpoints2 **ppEnum)  
{  
    HRESULT hRes = E_FAIL;  
  
    if ( ppEnum )  
    {  
        if ( m_pEnumBound )  
        {  
            hRes = m_pEnumBound->Clone(ppEnum);  
  
            if ( EVAL(S_OK == hRes) )  
                (*ppEnum)->Reset();  
        }  
        else  
            hRes = E_FAIL;  
    }  
    else  
        hRes = E_INVALIDARG;  
  
    return ( hRes );  
}  
```  
  
## See Also  
 [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md)   
 [IEnumDebugBoundBreakpoints2](../vs140/IEnumDebugBoundBreakpoints2.md)   
 [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md)