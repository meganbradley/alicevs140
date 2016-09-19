---
title: "PORT_SUPPLIER_DESCRIPTION_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5acee0ee-3a20-41c9-a7dc-0dadae6a5ba5
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PORT_SUPPLIER_DESCRIPTION_FLAGS
Defines the metadata that can be retrieved about a port supplier.  
  
## Syntax  
  
```cpp#  
enum enum_PORT_SUPPLIER_DESCRIPTION_FLAGS  
{  
   PSDFLAG_SHOW_WARNING_ICON = 0x1  
};  
typedef DWORD PORT_SUPPLIER_DESCRIPTION_FLAGS;  
```  
  
```c#  
public enum enum_PORT_SUPPLIER_DESCRIPTION_FLAGS  
{  
   PSDFLAG_SHOW_WARNING_ICON = 0x1  
};  
```  
  
## Terms  
 PSDFLAG_SHOW_WARNING_ICON  
 If selected, the warning icon will be displayed in the UI.  
  
## Remarks  
 This enumeration is returned by the [IDebugPortSupplierDescription2::GetDescription](../vs140/IDebugPortSupplierDescription2--GetDescription.md) method.  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugPortSupplierDescription2::GetDescription](../vs140/IDebugPortSupplierDescription2--GetDescription.md)