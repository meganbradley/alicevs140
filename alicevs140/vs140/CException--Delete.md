---
title: "CException::Delete"
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
ms.assetid: c0331586-4bf6-4ea3-86ca-3d999b6c6c58
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CException::Delete
This function checks to see if the **CException** object was created on the heap, and if so, it calls the **delete** operator on the object.  
  
## Syntax  
  
```  
  
void Delete( );  
  
```  
  
## Remarks  
 When deleting a **CException** object, use the **Delete** member function to delete the exception. Do not use the **delete** operator directly, because the `CException` object may be a global object or have been created on the stack.  
  
 You can specify whether the object should be deleted when the object is constructed. For more information, see [CException::CException](../vs140/CException--CException.md).  
  
 You only need to call **Delete** if you are using the C++ **try**-**catch** mechanism. If you are using the MFC macros **TRY** and **CATCH**, then these macros will automatically call this function.  
  
## Example  
 [!CODE [NVC_MFCExceptions#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#21)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CException Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)