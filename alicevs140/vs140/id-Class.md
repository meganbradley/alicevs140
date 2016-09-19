---
title: "id Class"
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
ms.assetid: 843fb25c-bb16-4f8e-aa9a-932f1e2fca60
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# id Class
The member class provides a unique facet identification used as an index for looking up facets in a locale.  
  
## Syntax  
  
```  
  
      class id {  
protected:  
   id( );  
private:  
   id(const id&)              // not defined  
   void operator=(const id&)  // not defined  
   };  
```  
  
## Remarks  
 The member class describes the static member object required by each unique locale facet. Note that you cannot copy or assign an object of class **id**.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [locale Class](../vs140/locale-Class.md)   
 [Thread Safety in the C++ Standard Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)