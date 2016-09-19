---
title: "AtlUnmarshalPtr"
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
ms.topic: reference
ms.assetid: 15d875dc-5132-4f72-a3dc-6640da0b709e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlUnmarshalPtr
Converts the stream's marshaling data into an interface pointer that can be used by the client.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT AtlUnmarshalPtr(  
IStream* pStream,  
const IID& iid,  
IUnknown** ppUnk   
);  
```  
  
#### Parameters  
 `pStream`  
 [in] A pointer to the stream being unmarshaled.  
  
 `iid`  
 [in] The GUID of the interface being unmarshaled.  
  
 `ppUnk`  
 [out] A pointer to the unmarshaled interface.  
  
## Return Value  
 A standard HRESULT value.  
  
## Example  
 See the example for [AtlMarshalPtrInProc](../vs140/AtlMarshalPtrInProc.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Marshaling Global Functions](../vs140/Marshaling-Global-Functions.md)   
 [AtlMarshalPtrInProc](../vs140/AtlMarshalPtrInProc.md)