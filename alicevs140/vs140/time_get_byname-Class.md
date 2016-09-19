---
title: "time_get_byname Class"
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
ms.assetid: 6e54153e-da40-4bb9-a942-1a6ce57b30c9
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# time_get_byname Class
The derived template class describes an object that can serve as a locale facet of type `time_get`<CharType, InputIterator>.  
  
## Syntax  
  
```  
template<class Elem, class InputIterator =   
   istreambuf_iterator<CharType, char_traits<CharType> > >  
   class time_get_byname : public time_get<CharType, InputIterator>  
{  
public:  
    explicit time_get_byname(  
        const char * _Locname,  
         size_t _Refs = 0  
    );  
    explicit time_get_byname(  
        const string& _Locname,  
        size_t _Refs = 0  
    );  
protected:  
    virtual ~time_get_byname()  
};  
```  
  
#### Parameters  
 `_Locname`  
 A named locale.  
  
 `_Refs`  
 An initial reference count.  
  
## Requirements  
 Its behavior is determined by the named locale `_Locname`. Each constructor initializes its base object with [time_get](../vs140/time_get-Class.md#time_get__time_get)<CharType, InputIterator>( `_Refs`).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)