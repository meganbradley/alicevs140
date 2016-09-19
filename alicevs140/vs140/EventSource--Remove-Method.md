---
title: "EventSource::Remove Method"
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
ms.assetid: afafedf5-3665-4408-a639-fb6884f7c5f9
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EventSource::Remove Method
Deletes the event handler represented by the specified event registration token from the set of event handlers associated with the current EventSource object.  
  
## Syntax  
  
```  
HRESULT Remove(  
   EventRegistrationToken token  
);  
```  
  
#### Parameters  
 `token`  
 A handle that represents an event handler. This token was returned when the event handler was registered by the [Add()](../vs140/EventSource--Add-Method.md) method.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Remarks  
 For more information about the EventRegistrationToken structure, see the Windows::Foundation::EventRegistrationToken Structure topic in the Windows Runtime reference documentation.  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [EventSource Class](../vs140/EventSource-Class.md)