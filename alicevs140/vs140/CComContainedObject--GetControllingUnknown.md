---
title: "CComContainedObject::GetControllingUnknown"
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
ms.assetid: 343ddb9a-483c-49b2-93a7-65e5f67c4c28
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComContainedObject::GetControllingUnknown
Returns the `m_pOuterUnknown` member pointer (inherited through the *Base* class) that holds the owner object's **IUnknown**.  
  
## Syntax  
  
```  
  
IUnknown* GetControllingUnknown( );  
  
```  
  
## Return Value  
 The owner object's **IUnknown**.  
  
## Remarks  
 This method may be virtual if `Base` has declared the [DECLARE_GET_CONTROLLING_UNKNOWN](../vs140/DECLARE_GET_CONTROLLING_UNKNOWN.md) macro.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComContainedObject Class](../vs140/CComContainedObject-Class.md)   
 [CComObjectRootEx::m_pOuterUnknown](../vs140/CComObjectRootEx--m_pOuterUnknown.md)