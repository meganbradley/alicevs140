---
title: "Container Class::erase"
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
ms.assetid: abc091c5-5a80-4bd8-93a8-a2d9bde2efec
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Container Class::erase
> [!NOTE]
>  This topic is in the Visual C++ documentation as a nonfunctional example of containers used in the Standard C++ Library. For more information, see [STL Containers](../vs140/STL-Containers.md).  
  
 Erases an element.  
  
## Syntax  
  
```  
  
      iterator erase(  
   iterator _Where   
);  
iterator erase(  
   iterator _First,  
   iterator _Last   
);  
```  
  
## Remarks  
 The first member function removes the element of the controlled sequence pointed to by _*Where***.** The second member function removes the elements of the controlled sequence in the range [`_First`, `_Last`). Both return an iterator that designates the first element remaining beyond any elements removed, or [end](../vs140/Container-Class--end.md) if no such element exists.  
  
 The member functions throw an exception only if a copy operation throws an exception.  
  
## See Also  
 [Sample Container Class](../vs140/Sample-Container-Class.md)