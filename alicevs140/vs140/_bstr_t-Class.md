---
title: "_bstr_t Class"
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
ms.topic: language-reference
ms.assetid: 58841fef-fe21-4a84-aab9-780262b5201f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _bstr_t Class
**Microsoft Specific**  
  
 A `_bstr_t` object encapsulates the [BSTR data type](assetId:///1b2d7d2c-47af-4389-a6b6-b01b7e915228). The class manages resource allocation and deallocation through function calls to **SysAllocString** and **SysFreeString** and other `BSTR` APIs when appropriate. The `_bstr_t` class uses reference counting to avoid excessive overhead.  
  
### Construction  
  
|||  
|-|-|  
|[_bstr_t](../vs140/_bstr_t--_bstr_t.md)|Constructs a `_bstr_t` object.|  
  
### Operations  
  
|||  
|-|-|  
|[Assign](../vs140/_bstr_t--Assign.md)|Copies a `BSTR` into the `BSTR` wrapped by a `_bstr_t`.|  
|[Attach](../vs140/_bstr_t--Attach.md)|Links a `_bstr_t` wrapper to a `BSTR`.|  
|[copy](../vs140/_bstr_t--copy.md)|Constructs a copy of the encapsulated `BSTR`.|  
|[Detach](../vs140/_bstr_t--Detach.md)|Returns the `BSTR` wrapped by a `_bstr_t` and detaches the `BSTR` from the `_bstr_t`.|  
|[GetAddress](../vs140/_bstr_t--GetAddress.md)|Points to the `BSTR` wrapped by a `_bstr_t`.|  
|[GetBSTR](../vs140/_bstr_t--GetBSTR.md)|Points to the beginning of the `BSTR` wrapped by the `_bstr_t`.|  
|[length](../vs140/_bstr_t--length.md)|Returns the number of characters in the `_bstr_t`.|  
  
### Operators  
  
|||  
|-|-|  
|[operator =](../vs140/_bstr_t--operator-=.md)|Assigns a new value to an existing `_bstr_t` object.|  
|[operator +=](../vs140/_bstr_t--operator--=---.md)|Appends characters to the end of the `_bstr_t` object.|  
|[operator +](../vs140/_bstr_t--operator--=---.md)|Concatenates two strings.|  
|[operator !](../vs140/_bstr_t--operator-!.md)|Checks if the encapsulated `BSTR` is a **NULL** string.|  
|[operator ==, !=, <, >, <=, >=](../vs140/_bstr_t-Relational-Operators.md)|Compares two `_bstr_t` objects.|  
|[operator wchar_t* &#124; char\*](../vs140/_bstr_t--wchar_t---_bstr_t--char-.md)|Extract the pointers to the encapsulated Unicode or multibyte `BSTR` object.|  
  
## END Microsoft Specific  
  
## Requirements  
 **Header:** comutil.h  
  
 **Lib:** comsuppw.lib or comsuppwd.lib (see [/Zc:wchar_t (wchar_t Is Native Type)](../Topic/-Zc:wchar_t%20\(wchar_t%20Is%20Native%20Type\).md) for more information)  
  
## See Also  
 [Compiler COM Support Classes](../vs140/Compiler-COM-Support-Classes.md)