---
title: "IDebugPendingBreakpoint2::Virtualize"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58c8e9a5-4494-47c2-bddb-56f628da6a2d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPendingBreakpoint2::Virtualize
Toggles the virtualized state of this pending breakpoint. When a pending breakpoint is virtualized, the debug engine will attempt to bind it every time new code loads into the program.  
  
## Syntax  
  
```cpp#  
HRESULT Virtualize(   
   BOOL fVirtualize  
);  
```  
  
```cpp#  
int Virtualize(   
   int fVirtualize  
);  
```  
  
#### Parameters  
 `fVirtualize`  
 [in] Set to nonzero (`TRUE`) to virtualize the pending breakpoint, or to zero (`FALSE`) to turn off virtualization.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_BP_DELETED` if the breakpoint has been deleted.  
  
## Remarks  
 A virtualized breakpoint is bound every time code is loaded.  
  
## Example  
 The following example shows how to implement this method for a simple `CPendingBreakpoint` object that exposes the [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) interface.  
  
```cpp#  
HRESULT CPendingBreakpoint::Virtualize(BOOL fVirtualize)    
{    
   HRESULT hr;    
  
   // Verify that the pending breakpoint has not been deleted. If deleted,   
   // then return hr = E_BP_DELETED.    
   if (m_state.state != PBPS_DELETED)    
   {    
      if (fVirtualize)    
      {    
         // Set the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         SetFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
      else    
      {    
         // Clear the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         ClearFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
      hr = S_OK;    
   }    
   else    
   {    
      hr = E_BP_DELETED;    
   }    
  
   return hr;    
}    
```  
  
## See Also  
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)