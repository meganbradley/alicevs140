---
title: "IDebugMethodField::GetThis"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc235bea-e909-4d8c-ab54-936736c803fc
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMethodField::GetThis
Gets the `this` (`Me` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) pointer of the object containing the method.  
  
## Syntax  
  
```cpp#  
HRESULT GetThis(   
   IDebugClassField** ppClass  
);  
```  
  
```c#  
int GetThis(  
   out IDebugClassField ppClass  
);  
```  
  
#### Parameters  
 `ppClass`  
 [out] Returns an [IDebugClassField](../vs140/IDebugClassField.md) object representing the "this" pointer.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 In object-oriented languages, there is typically an implied pointer to the current instantiation of a class. This is known as `this` in C#/C++ and as `Me` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].  
  
## See Also  
 [IDebugMethodField](../vs140/IDebugMethodField.md)   
 [IDebugClassField](../vs140/IDebugClassField.md)