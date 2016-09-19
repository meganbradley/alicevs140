---
title: "CString Semantics"
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
ms.assetid: d4023480-526f-499a-85f6-324b4de5b85f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CString Semantics
Even though [CString](../vs140/CStringT-Class.md) objects are dynamic objects that can grow, they act like built-in primitive types and simple classes. Each `CString` object represents a unique value. `CString` objects should be thought of as the actual strings rather than as pointers to strings.  
  
 You can assign one **CString** object to another. However, when you modify one of the two `CString` objects, the other `CString` object is not modified, as shown by the following example:  
  
 [!CODE [NVC_ATLMFC_Utilities#188](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#188)]  
  
 Note in the example that the two `CString` objects are considered "equal" because they represent the same character string. The `CString` class overloads the equality operator (`==`) to compare two `CString` objects based on their value (contents) rather than their identity (address).  
  
## See Also  
 [Strings (ATL/MFC)](../vs140/Strings--ATL-MFC-.md)