---
title: "basic_streambuf::imbue"
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
ms.assetid: 559a637f-116a-48be-9906-af0da589a243
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::imbue
A protected virtual function called by [pubimbue](../vs140/basic_streambuf--pubimbue.md).  
  
## Syntax  
  
```  
  
      virtual void imbue(  
   const locale &_Loc  
);  
```  
  
#### Parameters  
 `_Loc`  
 A reference to a locale.  
  
## Remarks  
 The default behavior is to do nothing.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)