---
title: "CA2CAEX Class"
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
ms.assetid: 388e7c1d-a144-474c-a182-b15f69a74bd8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2CAEX Class
This class is used by string conversion macros `CA2CTEX` and `CT2CAEX`, and the typedef **CA2CA**.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
   int  t_nBufferLength  
   = 128>  
   class CA2CAEX  
  
```  
  
#### Parameters  
 `t_nBufferLength`  
 The size of the buffer used in the translation process. The default length is 128 bytes.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CA2CAEX::CA2CAEX](../vs140/CA2CAEX--CA2CAEX.md)|The constructor.|  
|[CA2CAEX::~CA2CAEX](../vs140/CA2CAEX--~CA2CAEX.md)|The destructor.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CA2CAEX::operator LPCSTR](../vs140/CA2CAEX--operator-LPCSTR.md)|Conversion operator.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CA2CAEX::m_psz](../vs140/CA2CAEX--m_psz.md)|The data member that stores the source string.|  
  
## Remarks  
 Unless extra functionality is required, use `CA2CTEX`, `CT2CAEX`, or **CA2CA** in your own code.  
  
 This class is safe to use in loops and won't overflow the stack. By default, the ATL conversion classes and macros will use the current thread's ANSI code page for the conversion.  
  
 The following macros are based on this class:  
  
-   `CA2CTEX`  
  
-   `CT2CAEX`  
  
 The following typedef is based on this class:  
  
-   **CA2CA**  
  
 For a discussion of these text conversion macros, see [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md).  
  
## Example  
 See [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md) for an example of using these string conversion macros.  
  
## Requirements  
 **Header:** atlconv.h  
  
##  <a name="ca2caex__ca2caex"></a>  CA2CAEX::CA2CAEX  
 The constructor.  
  
```  
  
CA2CAEX(  
      LPCSTR  psz,  
      UINT  nCodePage  
   ) throw(...);  
   CA2CAEX(  
      LPCSTR  psz  
   ) throw(...);  
  
```  
  
### Parameters  
 `psz`  
 The text string to be converted.  
  
 `nCodePage`  
 Unused in this class.  
  
### Remarks  
 Creates the buffer required for the translation.  
  
##  <a name="ca2caex___dtorca2caex"></a>  CA2CAEX::~CA2CAEX  
 The destructor.  
  
```  
  
~CA2CAEX( ) throw( );  
  
```  
  
### Remarks  
 Frees the allocated buffer.  
  
##  <a name="ca2caex__m_psz"></a>  CA2CAEX::m_psz  
 The data member that stores the source string.  
  
```  
  
LPCSTR m_psz;  
  
```  
  
##  <a name="ca2caex__operator_lpcstr"></a>  CA2CAEX::operator LPCSTR  
 Conversion operator.  
  
```  
  
operator LPCSTR( ) const throw( );  
  
```  
  
### Return Value  
 Returns the text string as type `LPCSTR`.  
  
## See Also  
 [CA2AEX Class](../vs140/CA2AEX-Class.md)   
 [CA2WEX Class](../vs140/CA2WEX-Class.md)   
 [CW2AEX Class](../vs140/CW2AEX-Class.md)   
 [CW2CWEX Class](../vs140/CW2CWEX-Class.md)   
 [CW2WEX Class](../vs140/CW2WEX-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)