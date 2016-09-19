---
title: "IDiaStackWalkHelper::get_registerValue"
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
ms.assetid: 46ac5eee-73a3-44a1-8635-6c58ba193cb6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalkHelper::get_registerValue
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
 [in] A value from the [CV_HREG_e Enumeration](../vs140/CV_HREG_e.md) enumeration specifying which register to get the value from.  
  
 `pRetVal`  
 [out] Returns the current value of the register.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Despite the size of the `pRetVal` parameter, an implementation should store only what the register normally holds. For example, an 8-bit register holds only the lowest 8-bits of the given value. This 8-bit value is expanded to 64-bits when returned from this method.  
  
## See Also  
 [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md)   
 [CV_HREG_e Enumeration](../vs140/CV_HREG_e.md)