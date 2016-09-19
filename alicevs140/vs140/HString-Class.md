---
title: "HString Class"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 6709dd2e-8d72-4675-8ec7-1baa7d71854d
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HString Class
Provides support for manipulating HSTRING handles.  
  
## Syntax  
  
```cpp  
class HString;  
```  
  
## Remarks  
 The [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] provides access to strings through HSTRING handles. The HString class provides convenience functions and operators to simplify using HSTRING handles.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[HString::HStringConstructor](../vs140/HString--HString-Constructor.md)|Initializes a new instance of the HString class.|  
|[HString::~HStringConstructor](../vs140/HString--~HString-Destructor.md)|Destroys the current instance of the HString class.|  
  
### Members  
  
|Name|Description|  
|----------|-----------------|  
|[HString::Set Method](../vs140/HString--Set-Method.md)|Sets the value of the current HString object to the specified wide-character string or HString parameter.|  
|[HString::Attach Method](../vs140/HString--Attach-Method.md)|Associates the specified HString object with the current HString object.|  
|[HString::CopyTo Method](../vs140/HString--CopyTo-Method.md)|Copies the current HString object to an HSTRING object.|  
|[HString::Detach Method](../vs140/HString--Detach-Method.md)|Disassociates the specified HString object from its underlying value.|  
|[HString::GetAddressOf Method](../vs140/HString--GetAddressOf-Method.md)|Retrieves a pointer to the underlying HSTRING handle.|  
|[HString::Get Method](../vs140/HString--Get-Method.md)|Retrieves the value of the underlying HSTRING handle.|  
|[HString::Release Method](../vs140/HString--Release-Method.md)|Deletes the underlying string value and intializes the current HString object to an empty value.|  
|[HString::MakeReference Method](../vs140/HString--MakeReference-Method.md)|Creates an HStringReference object from a specified string parameter.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[operator=](../vs140/HString--Operator=-Operator.md)|Moves the value of another HString object to the current HString object.|  
|[operator==](../vs140/HString--Operator==-Operator.md)|Indicates whether the two parameters are equal.|  
|[operator!=](../vs140/HString--Operator!=-Operator.md)|Indicates whether the two parameters are not equal.|  
  
## Inheritance Hierarchy  
 `HString`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)