---
title: "IDebugClassField::EnumInterfacesImplemented"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5523e45-d350-491e-a92c-fe0ca97d2052
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugClassField::EnumInterfacesImplemented
Creates an enumerator for the interfaces implemented by this class.  
  
## Syntax  
  
```cpp#  
HRESULT EnumInterfacesImplemented(   
   IEnumDebugFields** ppEnum  
);  
```  
  
```c#  
int EnumInterfacesImplemented(  
   out IEnumDebugFields ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugFields](../vs140/IEnumDebugFields.md) object representing the list of interfaces implemented. Returns a null value if there are no interfaces.  
  
## Return Value  
 If successful, returns S_OK or returns S_FALSE if there are no interfaces implemented on this class. Otherwise, returns an error code.  
  
## Remarks  
 Each element of the enumeration is an [IDebugClassField](../vs140/IDebugClassField.md) object describing an interface. Note that unmanaged [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] code does not use interfaces as a discrete entity so this method always returns a null value for unmanaged [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] code.  
  
## See Also  
 [IDebugClassField](../vs140/IDebugClassField.md)   
 [IEnumDebugFields](../vs140/IEnumDebugFields.md)