---
title: "FIELD_INFO_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a69487d2-e701-4165-804a-8a011df9a3bd
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# FIELD_INFO_FIELDS
Specifies what information to retrieve about an [IDebugField](../vs140/IDebugField.md) object.  
  
## Syntax  
  
```cpp#  
enum enum_FIELD_INFO_FIELDS {   
   FIF_FULLNAME  = 0x0001,  
   FIF_NAME      = 0x0002,  
   FIF_TYPE      = 0x0004,  
   FIF_MODIFIERS = 0x0008,  
   FIF_ALL       = 0xffffffff,  
   FIF_NONE      = 0x0000  
};  
typedef DWORD FIELD_INFO_FIELDS;  
```  
  
```c#  
public enum enum_FIELD_INFO_FIELDS {  
   FIF_FULLNAME  = 0x0001,  
   FIF_NAME      = 0x0002,  
   FIF_TYPE      = 0x0004,  
   FIF_MODIFIERS = 0x0008,  
   FIF_ALL       = 0xffffffff,  
   FIF_NONE      = 0x0000  
};  
```  
  
## Members  
 FIF_FULLNAME  
 Initialize/use the `bstrFullName` field in the [FIELD_INFO](../vs140/FIELD_INFO.md) structure.  
  
 FIF_NAME  
 Initialize/use the `bstrName` field in the `FIELD_INFO` structure.  
  
 FIF_TYPE  
 Initialize/use the `bstrType` field in the `FIELD_INFO` structure.  
  
 FIF_MODIFIERS  
 Initialize/use the `bstrModifiers` field in the `FIELD_INFO` structure.  
  
## Remarks  
 These values are also passed as an argument to the [GetInfo](../vs140/IDebugField--GetInfo.md) method to specify which fields of the [FIELD_INFO](../vs140/FIELD_INFO.md) structure are to be initialized.  
  
 These values are also used in the `dwFields` member of the `FIELD_INFO` structure to indicate which fields are used and valid.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [FIELD_INFO](../vs140/FIELD_INFO.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [GetInfo](../vs140/IDebugField--GetInfo.md)