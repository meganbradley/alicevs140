---
title: "StackFrameTypeEnum"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61e40163-eee0-4c1f-af47-cef3771bdc41
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# StackFrameTypeEnum
Specifies the stack frame type.  
  
## Syntax  
  
```cpp  
enum StackFrameTypeEnum {  
   FrameTypeFPO,  
   FrameTypeTrap,  
   FrameTypeTSS,  
   FrameTypeStandard,  
   FrameTypeFrameData,  
   FrameTypeUnknown = -1  
};  
```  
  
## Elements  
 `FrameTypeFPO`  
 Frame pointer omitted; FPO info available.  
  
 `FrameTypeTrap`  
 Kernel Trap frame.  
  
 `FrameTypeTSS`  
 Kernel Trap frame.  
  
 `FrameTypeStandard`  
 Standard EBP stack frame.  
  
 `FrameTypeFrameData`  
 Frame pointer omitted; Frame data info available.  
  
 `FrameTypeUnknown`  
 Frame that does not have any debug info.  
  
## Remarks  
 The values in this enumeration are returned by a call to the [IDiaStackFrame::get_type](../vs140/IDiaStackFrame--get_type.md) method.  
  
## Requirements  
 Header: cvconst.h  
  
## See Also  
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)   
 [IDiaStackFrame::get_type](../vs140/IDiaStackFrame--get_type.md)