---
title: "IDebugEngine2::CreatePendingBreakpoint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92e85b90-a931-48d9-89a7-a6edcb83ae5a
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine2::CreatePendingBreakpoint
Creates a pending breakpoint in the debug engine (DE).  
  
## Syntax  
  
```cpp#  
HRESULT CreatePendingBreakpoint(   
   IDebugBreakpointRequest2*  pBPRequest,  
   IDebugPendingBreakpoint2** ppPendingBP  
);  
```  
  
```c#  
int CreatePendingBreakpoint(   
   IDebugBreakpointRequest2     pBPRequest,  
   out IDebugPendingBreakpoint2 ppPendingBP  
);  
```  
  
#### Parameters  
 `pBPRequest`  
 [in] An [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md) object that describes the pending breakpoint to create.  
  
 `ppPendingBP`  
 [out] Returns an [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) object that represents the pending breakpoint.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Typically returns `E_FAIL` if the `pBPRequest` parameter does not match any language supported by the DE of if the `pBPRequest` parameter is invalid or incomplete.  
  
## Remarks  
 A pending breakpoint is essentially a collection of all the information needed to bind a breakpoint to code. The pending breakpoint returned from this method is not bound to code until the [Bind](../vs140/IDebugPendingBreakpoint2--Bind.md) method is called.  
  
 For each pending breakpoint the user sets, the session debug manager (SDM) calls this method in each attached DE. It is up to the DE to verify that the breakpoint is valid for programs running in that DE.  
  
 When the user sets a breakpoint on a line of code, the DE is free to bind the breakpoint to the closest line in the document that corresponds to this code. This makes it possible for the user to set a breakpoint on the first line of a multi-line statement, but bind it on the last line (where all the code is attributed in the debug information).  
  
## Example  
 The following example shows how to implement this method for a simple `CProgram` object. The DE's implementation of the `IDebugEngine2::CreatePendingBreakpoint` could then forward all calls to this implementation of the method in each program.  
  
```  
HRESULT CProgram::CreatePendingBreakpoint(IDebugBreakpointRequest2* pBPRequest, IDebugPendingBreakpoint2** ppPendingBP)     
{    
  
   // Create and initialize the CPendingBreakpoint object.  
   CComObject<CPendingBreakpoint> *pPending;    
   CComObject<CPendingBreakpoint>::CreateInstance(&pPending);    
   pPending->Initialize(pBPRequest, m_pInterp, m_pCallback, m_pEngine);    
   return pPending->QueryInterface(ppPendingBP);    
}    
```  
  
## See Also  
 [IDebugEngine2](../vs140/IDebugEngine2.md)   
 [Bind](../vs140/IDebugPendingBreakpoint2--Bind.md)   
 [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)