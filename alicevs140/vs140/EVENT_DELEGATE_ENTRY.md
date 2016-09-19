---
title: "EVENT_DELEGATE_ENTRY"
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
ms.topic: article
ms.assetid: 17539da5-bad7-43ff-8a54-6ea3dc564965
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EVENT_DELEGATE_ENTRY
Creates an entry in the delegate map.  
  
## Syntax  
  
```  
EVENT_DELEGATE_ENTRY(  
   MEMBER,  
   ARG0,  
   ARG1  
);  
```  
  
#### Parameters  
 `MEMBER`  
 The event handler method to be attached to the control.  
  
 `ARG0`  
 The first argument of the managed event handler method, such as **Object^**.  
  
 `ARG1`  
 The second argument of the managed event handler method, such as **EventArgs^**.  
  
## Remarks  
 Each entry in the delegate map corresponds to a managed event handler delegate created by [MAKE_DELEGATE](../vs140/MAKE_DELEGATE.md).  
  
## Example  
 The following code example shows how to use `EVENT_DELEGATE_ENTRY` to create an entry in the delegate map for the `OnClick` event handler; also see the code example in `MAKE_DELEGATE`. For more information, see [How To: Sink Windows Forms Events from Native C++ Classes](../Topic/How%20to:%20Sink%20Windows%20Forms%20Events%20from%20Native%20C++%20Classes.md).  
  
 [!CODE [NVC_MFC_Managed#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Managed#5)]  
  
## Requirements  
 **Header:** msclr\event.h  
  
## See Also  
 [MAKE_DELEGATE](../vs140/MAKE_DELEGATE.md)   
 [BEGIN_DELEGATE_MAP](../vs140/BEGIN_DELEGATE_MAP.md)   
 [END_DELEGATE_MAP](../vs140/END_DELEGATE_MAP.md)