---
title: "IDiaStackWalkFrame::get_registerValue"
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
ms.assetid: ca3c20a9-934a-4b2c-a7f6-7d06e8611ff2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalkFrame::get_registerValue
Retrieves the value of a register.  
  
## Syntax  
  
```cpp#  
HRESULT get_registerValue (   
   DWORD      index,  
   ULONGLONG* pRetVal  
);  
```  
  
#### Parameters  
 `index`  
 [in] A value from the [CV_HREG_e Enumeration](../vs140/CV_HREG_e.md) enumeration specifying the register to get the value for.  
  
 `pRetVal`  
 [out] Returns the current value of the register.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaStackWalkFrame](../vs140/IDiaStackWalkFrame.md)   
 [CV_HREG_e Enumeration](../vs140/CV_HREG_e.md)