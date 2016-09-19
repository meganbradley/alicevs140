---
title: "CFixedStringT Class"
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
ms.assetid: 6d4171ba-3104-493a-a6cc-d515f4ba9a4b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFixedStringT Class
This class represents a string object with a fixed character buffer.  
  
## Syntax  
  
```  
  
template< class   
StringType  
, int   
t_nChars  
 >    
class CFixedStringT : private CFixedStringMgr, public StringType  
  
```  
  
#### Parameters  
 `StringType`  
 Used as the base class for the fixed string object and can be any                         `CStringT`-based type. Some examples include                         `CString`,                         `CStringA`, and                         `CStringW`.  
  
 *t_nChars*  
 The number of characters stored in the buffer.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CFixedStringT::CFixedStringT](#cfixedstringt__cfixedstringt)|The constructor for the string object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CFixedStringT::operator =](#cfixedstringt__operator__eq)|Assigns a new value to a                                         `CFixedStringT` object.|  
  
## Remarks  
 This class is an example of a custom string class based on                 `CStringT`. Although quite similar, the two classes differ in implementation. The major differences between                 `CFixedStringT` and                 `CStringT` are:  
  
-   The initial character buffer is allocated as part of the object and has size                         *t_nChars*. This allows the                         **CFixedString** object to occupy a contiguous memory chunk for performance purposes. However, if the contents of a                         `CFixedStringT` object grows beyond                         *t_nChars*, the buffer is allocated dynamically.  
  
-   The character buffer for a                         `CFixedStringT` object is always the same length (                        *t_nChars*). There is no limitation on buffer size for                         `CStringT` objects.  
  
-   The memory manager for                         `CFixedStringT` is customized such that sharing of a                         [CStringData](../vs140/CStringData-Class.md) object between two or more                         `CFixedStringT` objectsis not allowed.                         `CStringT` objects do not have this limitation.  
  
 For more information on the customization of                 `CFixedStringT` and memory management for string objects in general, see                 [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Inheritance Hierarchy  
 `IAtlStringMgr`  
  
 `StringType`  
  
 `CFixedStringMgr`  
  
 `CFixedStringT`  
  
## Requirements  
 **Header:** cstringt.h  
  
##  <a name="cfixedstringt__cfixedstringt"></a>  CFixedStringT::CFixedStringT  
 Constructs a                 `CFixedStringT` object.  
  
```  
  
CFixedStringT( ) throw( );   
explicit CFixedStringT(  
   IAtlStringMgr*   
pStringMgr  
) throw( );  
CFixedStringT(  
   const CFixedStringT< StringType,  
t_nChars >&   
str  
);  
CFixedStringT(  
   const StringType&   
str  
);  
CFixedStringT(  
   const StringType::XCHAR*   
psz  
);  
explicit CFixedStringT(  
   const StringType::YCHAR*   
psz  
);  
explicit CFixedStringT(  
   const unsigned char*   
psz  
);  
  
```  
  
### Parameters  
 `psz`  
 A null-terminated string to be copied into this                                 `CFixedStringT` object.  
  
 `str`  
 An existing                                 `CFixedStringT` object to be copied into this                                 `CFixedStringT` object.  
  
 `pStringMgr`  
 A pointer to the memory manager of the                                 `CFixedStringT` object. For more information on                                 `IAtlStringMgr` and memory management for                                 `CFixedStringT`, see                                 [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
### Remarks  
 Because the constructors copy the input data into new allocated storage, you should be aware that memory exceptions may result. Note that some of these constructors act as conversion functions.  
  
##  <a name="cfixedstringt__operator__eq"></a>  CFixedStringT::operator =  
 Reinitializes an existing                 `CFixedStringT` object with new data.  
  
```  
  
CFixedStringT< StringType,  
t_nChars >& operator =(  
   const CFixedStringT< StringType,  
t_nChars >&   
str  
);  
CFixedStringT< StringType,  
t_nChars >& operator =(  
   const char*   
psz  
);  
CFixedStringT< StringType,  
t_nChars >& operator =(  
   const wchar_t*   
psz  
);  
CFixedStringT< StringType,  
t_nChars >& operator =(  
   const unsigned char*   
psz  
);  
CFixedStringT< StringType, t_nChars >& operator =(  
   const StringType&   
str  
);  
  
```  
  
### Parameters  
 `str`  
 A null-terminated string to be copied into this                                 `CFixedStringT` object.  
  
 `psz`  
 An existing                                 `CFixedStringT` to be copied into this                                 `CFixedStringT` object.  
  
### Remarks  
 You should be aware that memory exceptions may occur whenever you use the assignment operator because new storage is often allocated to hold the resulting                         `CFixedStringT` object.  
  
## See Also  
 [CStringT](../vs140/CStringT-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Shared Classes](../vs140/ATL-MFC-Shared-Classes.md)