---
title: "IDebugExtendedField::IsClosedType"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9136fc57-74ff-4fe4-a6e2-b137cb9d5b08
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExtendedField::IsClosedType
Determines if the field represents a closed type.  
  
## Syntax  
  
```cpp#  
HRESULT IsClosedType(  
   void  
);  
```  
  
```c#  
int IsClosedType();  
```  
  
## Return Value  
 If the field is a closed type, returns `S_OK`; otherwise, returns `S_FALSE`.  
  
## See Also  
 [IDebugExtendedField](../vs140/IDebugExtendedField.md)