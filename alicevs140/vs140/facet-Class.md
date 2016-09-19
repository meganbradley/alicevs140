---
title: "facet Class"
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
ms.assetid: dd4f12f5-cb1b-457f-af56-2fb204216ec1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# facet Class
A class that serves as the base class for all locale facets.  
  
## Syntax  
  
```  
  
      class facet {  
protected:  
   explicit facet(  
      size_t _Refs = 0  
);  
   virtual ~facet( );  
private:  
   facet(const facet&)           // not defined  
   void operator=(const facet&)  // not defined  
   };  
```  
  
## Remarks  
 Note that you cannot copy or assign an object of class facet. You can construct and destroy objects derived from class `locale::facet` but not objects of the base class proper. Typically, you construct an object `_Myfac` derived from facet when you construct a locale, as in **locale loc**(`locale::classic`( ), **new** `_Myfac`);  
  
 In such cases, the constructor for the base class facet should have a zero `_Refs` argument. When the object is no longer needed, it is deleted. Thus, you supply a nonzero _*Refs* argument only in those rare cases where you take responsibility for the lifetime of the object.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [locale Class](../vs140/locale-Class.md)   
 [Thread Safety in the C++ Standard Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)