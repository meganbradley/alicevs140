---
title: "DataKind"
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
ms.assetid: b64be708-22d6-4360-99e7-8f4e6b196de7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DataKind
Indicates the particular scope of a data value.  
  
## Syntax  
  
```cpp#  
enum DataKind {   
   DataIsUnknown,  
   DataIsLocal,  
   DataIsStaticLocal,  
   DataIsParam,  
   DataIsObjectPtr,  
   DataIsFileStatic,  
   DataIsGlobal,  
   DataIsMember,  
   DataIsStaticMember,  
   DataIsConstant  
};  
```  
  
## Elements  
 DataIsUnknown  
 Data symbol cannot be determined.  
  
 DataIsLocal  
 Data item is a local variable.  
  
 DataIsStaticLocal  
 Data item is a static local variable.  
  
 DataIsParam  
 Data item is a formal parameter.  
  
 DataIsObjectPtr  
 Data item is an object pointer (`this`).  
  
 DataIsFileStatic  
 Data item is a file-scoped variable.  
  
 DataIsGlobal  
 Data item is a global variable.  
  
 DataIsMember  
 Data item is an object member variable.  
  
 DataIsStaticMember  
 Data item is a class static variable.  
  
 DataIsConstant  
 Data item is a constant value.  
  
## Remarks  
 The values in this enumeration are returned by the [IDiaSymbol::get_dataKind](../vs140/IDiaSymbol--get_dataKind.md) method.  
  
## Requirements  
 Header: cvconst.h  
  
## See Also  
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)   
 [IDiaSymbol::get_dataKind](../vs140/IDiaSymbol--get_dataKind.md)