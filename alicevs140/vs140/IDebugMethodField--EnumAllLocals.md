---
title: "IDebugMethodField::EnumAllLocals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0bc7cc13-2628-4bd8-8c06-4d2aa6755ea8
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMethodField::EnumAllLocals
Creates an enumerator for all local variables of the method, including those generated internally by a compiler.  
  
## Syntax  
  
```cpp#  
HRESULT EnumAllLocals(   
   IDebugAddress*     pAddress,  
   IEnumDebugFields** ppLocals  
);  
```  
  
```c#  
int EnumAllLocals(  
   IDebugAddress        pAddress,   
   out IEnumDebugFields ppLocals  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] An [IDebugAddress](../vs140/IDebugAddress.md) object representing a debug address within the method, pointing to a particular scope or context.  
  
 `ppLocals`  
 [out] Returns an [IEnumDebugFields](../vs140/IEnumDebugFields.md) object representing the list of all locals in the specified scope; otherwise, returns a null value indicating no locals.  
  
## Return Value  
 If successful, returns S_OK or returns S_FALSE if there are no locals. Otherwise, returns an error code.  
  
## Remarks  
 Only the variables defined within the block that contains the given debug address are enumerated. This method includes any compiler-generated locals. If all that is needed are the locals explicitly defined in the source, call the [IDebugMethodField::EnumLocals](../vs140/IDebugMethodField--EnumLocals.md) method.  
  
 A method can contain multiple scoping contexts or blocks.  
  
## See Also  
 [IDebugMethodField](../vs140/IDebugMethodField.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)   
 [IEnumDebugFields](../vs140/IEnumDebugFields.md)   
 [IDebugMethodField::EnumLocals](../vs140/IDebugMethodField--EnumLocals.md)