---
title: "IDebugField::GetContainer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d6c8213-6181-4adf-9584-3e4cac163dd8
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugField::GetContainer
This method gets the container of a field.  
  
## Syntax  
  
```cpp#  
HRESULT GetContainer(   
   IDebugContainerField** ppContainerField  
);  
```  
  
```c#  
int GetContainer(  
   out IDebugContainerField ppContainerField  
);  
```  
  
#### Parameters  
 `ppContainerField`  
 [out] Returns the container as represented by the [IDebugContainerField](../vs140/IDebugContainerField.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 If this field does not have a container, the returned `ppContainerField` will be a null value.  
  
## See Also  
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)