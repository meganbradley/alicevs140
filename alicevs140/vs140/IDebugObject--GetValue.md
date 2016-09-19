---
title: "IDebugObject::GetValue"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eec6051e-8ecb-49fa-bdd4-dd786f211692
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject::GetValue
Gets the value of the object as a consecutive series of bytes.  
  
## Syntax  
  
```cpp#  
HRESULT GetValue(   
   BYTE* pValue,  
   UINT  nSize  
);  
```  
  
```c#  
int GetValue(  
   ref byte[] pValue,   
   uint nSize  
);  
```  
  
#### Parameters  
 `pValue`  
 [in, out] An array that is filled in with a consecutive series of bytes representing the value of the object.  
  
 `nSize`  
 [in] The maximum number of bytes to fetch.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Get the total number of value bytes that can be fetched by calling the [IDebugObject::GetSize](../vs140/IDebugObject--GetSize.md) method.  
  
## See Also  
 [IDebugObject](../vs140/IDebugObject.md)