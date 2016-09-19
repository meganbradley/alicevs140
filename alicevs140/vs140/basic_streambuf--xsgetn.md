---
title: "basic_streambuf::xsgetn"
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
ms.assetid: 39d26568-eb2e-485f-b7f5-a83738dfcef6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::xsgetn
Protected, virtual function to extract elements from the input stream.  
  
 This method is potentially unsafe, as it relies on the caller to check that the passed values are correct.  
  
## Syntax  
  
```  
virtual streamsize xsgetn(  
   char_type *_Ptr,  
   streamsize _Count  
);  
```  
  
#### Parameters  
 `_Ptr`  
 The buffer to contain the extracted characters.  
  
 `_Count`  
 The number of elements to extract.  
  
## Return Value  
 The number of elements extracted.  
  
## Remarks  
 The protected virtual member function extracts up to `_Count` elements from the input stream, as if by repeated calls to [sbumpc](../vs140/basic_streambuf--sbumpc.md), and stores them in the array beginning at `_Ptr`. It returns the number of elements actually extracted.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)