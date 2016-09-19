---
title: "Chained Unwind Info Structures"
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
ms.topic: article
ms.assetid: 176835bf-f118-45d9-9128-9db4b7571864
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Chained Unwind Info Structures
If the UNW_FLAG_CHAININFO flag is set, then an unwind info structure is a secondary one, and the shared exception-handler/chained-info address field contains the primary unwind information. The following code retrieves the primary unwind information, assuming that `unwindInfo` is the structure that has the UNW_FLAG_CHAININFO flag set.  
  
```  
PRUNTIME_FUNCTION primaryUwindInfo = (PRUNTIME_FUNCTION)&(unwindInfo->UnwindCode[( unwindInfo->CountOfCodes + 1 ) & ~1]);  
```  
  
 Chained info is useful in two situations. First, it can be used for noncontiguous code segments. By using chained info, you can reduce the size of the required unwind information, because you do not have to duplicate the unwind codes array from the primary unwind info.  
  
 You can also use chained info to group volatile register saves. The compiler may delay saving some volatile registers until it is outside of the function entry prolog. You can record this by having primary unwind info for the portion of the function before the grouped code, and then setting up chained info with a non-zero size of prolog, where the unwind codes in the chained info reflect saves of the nonvolatile registers. In that case, the unwind codes are all instances of UWOP_SAVE_NONVOL. A grouping that saves nonvolatile registers by using a PUSH or modifies the RSP register by using an additional fixed stack allocation is not supported.  
  
 An UNWIND_INFO item that has UNW_FLAG_CHAININFO set can contain a RUNTIME_FUNCTION entry whose UNWIND_INFO item also has UNW_FLAG_CHAININFO set (multiple shrink-wrapping). Eventually, the chained unwind info pointers will arrive at an UNWIND_INFO item that has UNW_FLAG_CHAININFO cleared; this is the primary UNWIND_INFO item, which points to the actual procedure entry point.  
  
## See Also  
 [Unwind Data for Exception Handling, Debugger Support](../vs140/Unwind-Data-for-Exception-Handling--Debugger-Support.md)