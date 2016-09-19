---
title: "IDebugCustomAttributeQuery2::EnumCustomAttributes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94bfce74-aa3d-45f0-8e04-5715faf85217
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttributeQuery2::EnumCustomAttributes
Gets an enumerator for all custom attributes attached to this field.  
  
## Syntax  
  
```cpp#  
HRESULT EnumCustomAttributes(   
   IEnumDebugCustomAttributes** ppEnum  
);  
```  
  
```c#  
int EnumCustomAttributes(  
   out IEnumDebugCustomAttributes ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugCustomAttributes](../vs140/IEnumDebugCustomAttributes.md) object representing the list of custom attributes; otherwise, returns a null value if there are no custom attributes.  
  
## Return Value  
 If successful, returns S_OK or S_FALSE if there are no custom attributes on this field. Otherwise, returns an error code;  
  
## Remarks  
 A field can have multiple custom attributes.  
  
## See Also  
 [IDebugCustomAttributeQuery2](../vs140/IDebugCustomAttributeQuery2.md)   
 [IEnumDebugCustomAttributes](../vs140/IEnumDebugCustomAttributes.md)