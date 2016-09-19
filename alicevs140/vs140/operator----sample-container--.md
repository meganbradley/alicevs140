---
title: "operator&lt; (&lt;sample container&gt;)"
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
ms.assetid: 31027dd6-53be-428b-b950-1dcb25393597
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt; (&lt;sample container&gt;)
> [!NOTE]
>  This topic is in the Visual C++ documentation as a nonfunctional example of containers used in the Standard C++ Library. For more information, see [STL Containers](../vs140/STL-Containers.md).  
  
 Overloads **operator<** to compare two objects of template class [Container](../vs140/Sample-Container-Class.md).  
  
## Syntax  
  
```  
  
   template<class Ty>  
bool operator<(  
   const Container <Ty>& _Left,  
   const Container <Ty>& _Right  
);  
```  
  
## Return Value  
 Returns `lexicographical_compare`(_*Left*. [begin](../vs140/Container-Class--begin.md), \_*Left*. [end](../vs140/Container-Class--end.md), \_*Right***.begin**, \_*Right*.**end**).  
  
## See Also  
 [<sample container\>](../vs140/-sample-container-.md)