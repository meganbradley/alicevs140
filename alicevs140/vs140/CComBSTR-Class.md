---
title: "CComBSTR Class"
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
ms.assetid: 8fea1879-a05e-47a5-a803-8dec60eaa534
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR Class
This class is a wrapper for `BSTR`s.  
  
## Syntax  
  
```  
  
class CComBSTR  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComBSTR::CComBSTR](../vs140/CComBSTR--CComBSTR.md)|The constructor.|  
|[CComBSTR::~CComBSTR](../vs140/CComBSTR--~CComBSTR.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComBSTR::Append](../vs140/CComBSTR--Append.md)|Appends a string to `m_str`.|  
|[CComBSTR::AppendBSTR](../vs140/CComBSTR--AppendBSTR.md)|Appends a `BSTR` to `m_str`.|  
|[CComBSTR::AppendBytes](../vs140/CComBSTR--AppendBytes.md)|Appends a specified number of bytes to `m_str`.|  
|[CComBSTR::ArrayToBSTR](../vs140/CComBSTR--ArrayToBSTR.md)|Creates a `BSTR` from the first character of each element in the safearray and attaches it to the `CComBSTR` object.|  
|[CComBSTR::AssignBSTR](../vs140/CComBSTR--AssignBSTR.md)|Assigns a `BSTR` to `m_str`.|  
|[CComBSTR::Attach](../vs140/CComBSTR--Attach.md)|Attaches a `BSTR` to the `CComBSTR` object.|  
|[CComBSTR::BSTRToArray](../vs140/CComBSTR--BSTRToArray.md)|Creates a zero-based one-dimensional safearray, where each element of the array is a character from the `CComBSTR` object.|  
|[CComBSTR::ByteLength](../vs140/CComBSTR--ByteLength.md)|Returns the length of `m_str` in bytes.|  
|[CComBSTR::Copy](../vs140/CComBSTR--Copy.md)|Returns a copy of `m_str`.|  
|[CComBSTR::CopyTo](../vs140/CComBSTR--CopyTo.md)|Returns a copy of `m_str` via an **[out]** parameter|  
|[CComBSTR::Detach](../vs140/CComBSTR--Detach.md)|Detaches `m_str` from the `CComBSTR` object.|  
|[CComBSTR::Empty](../vs140/CComBSTR--Empty.md)|Frees `m_str`.|  
|[CComBSTR::Length](../vs140/CComBSTR--Length.md)|Returns the length of `m_str`.|  
|[CComBSTR::LoadString](../vs140/CComBSTR--LoadString.md)|Loads a string resource.|  
|[CComBSTR::ReadFromStream](../vs140/CComBSTR--ReadFromStream.md)|Loads a `BSTR` object from a stream.|  
|[CComBSTR::ToLower](../vs140/CComBSTR--ToLower.md)|Converts the string to lowercase.|  
|[CComBSTR::ToUpper](../vs140/CComBSTR--ToUpper.md)|Converts the string to uppercase.|  
|[CComBSTR::WriteToStream](../vs140/CComBSTR--WriteToStream.md)|Saves `m_str` to a stream.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CComBSTR::operator BSTR](../vs140/CComBSTR--operator-BSTR.md)|Casts a `CComBSTR` object to a `BSTR`.|  
|[CComBSTR::operator !](../vs140/CComBSTR--operator-!.md)|Returns `true` or `false`, depending on whether `m_str`is `NULL`.|  
|[CComBSTR::operator !=](../vs140/CComBSTR--operator-!=.md)|Compares a `CComBSTR` with a string.|  
|[CComBSTR::operator &](../vs140/CComBSTR--operator--.md)|Returns the address of `m_str`.|  
|[CComBSTR::operator +=](../vs140/CComBSTR--operator--=.md)|Appends a `CComBSTR` to the object.|  
|[CComBSTR::operator <](../vs140/CComBSTR--operator--.md)|Compares a `CComBSTR` with a string.|  
|[CComBSTR::operator =](../vs140/CComBSTR--operator-=.md)|Assigns a value to `m_str`.|  
|[CComBSTR::operator ==](../vs140/CComBSTR--operator-==.md)|Compares a `CComBSTR` with a string.|  
|[CComBSTR::operator >](../vs140/CComBSTR--operator--.md)|Compares a `CComBSTR` with a string.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComBSTR::m_str](../vs140/CComBSTR--m_str.md)|Contains the `BSTR` associated with the `CComBSTR` object.|  
  
## Remarks  
 The `CComBSTR` class is a wrapper for `BSTR`s, which are length-prefixed strings. The length is stored as an integer at the memory location preceding the data in the string.  
  
 A [BSTR](assetId:///1b2d7d2c-47af-4389-a6b6-b01b7e915228) is null-terminated after the last counted character but may also contain null characters embedded within the string. The string length is determined by the character count, not the first null character.  
  
> [!NOTE]
>  The `CComBSTR` class provides a number of members (constructors, assignment operators, and comparison operators) that take either ANSI or Unicode strings as arguments. The ANSI versions of these functions are less efficient than their Unicode counterparts because temporary Unicode strings are often created internally. For efficiency, use the Unicode versions where possible.  
  
> [!NOTE]
>  Because of the improved lookup behavior implemented in Visual Studio .NET, code such as `bstr = L"String2" + bstr;`, which may have compiled in previous releases, should instead be implemented as `bstr = CStringW(L"String2") + bstr`.  
  
 For a list of cautions when using `CComBSTR`, see [Programming with CComBSTR](../vs140/Programming-with-CComBSTR--ATL-.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="ccombstr__append"></a>  CComBSTR::Append  
 Appends either `lpsz` or the `BSTR` member of `bstrSrc` to [m_str](../vs140/CComBSTR--m_str.md).  
  
```  
  
HRESULT Append(  
      const CComBSTR&  bstrSrc  
   ) throw( );  
   HRESULT Append(  
      wchar_t  ch  
   ) throw( );  
   HRESULT Append(  
      char  ch  
   ) throw( );  
   HRESULT Append(  
      LPCOLESTR  lpsz  
   ) throw( );  
   HRESULT Append(  
      LPCSTR  lpsz  
   ) throw( );  
   HRESULT Append(  
      LPCOLESTR  lpsz,  
      int  nLen  
   ) throw( );  
  
```  
  
### Parameters  
 `bstrSrc`  
 [in] A `CComBSTR` object to append.  
  
 *ch*  
 [in] A character to append.  
  
 `lpsz`  
 [in] A zero-terminated character string to append. You can pass a Unicode string via the **LPCOLESTR** overload or an ANSI string via the `LPCSTR` version.  
  
 `nLen`  
 [in] The number of characters from `lpsz` to append.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
### Remarks  
 An ANSI string will be converted to Unicode before being appended.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#32](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#32)]  
  
##  <a name="ccombstr__appendbstr"></a>  CComBSTR::AppendBSTR  
 Appends the specified `BSTR` to [m_str](../vs140/CComBSTR--m_str.md).  
  
```  
  
HRESULT AppendBSTR(  
      BSTR  p  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 [in] A `BSTR` to append.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
### Remarks  
 Do not pass an ordinary wide-character string to this method. The compiler cannot catch the error and run time errors will occur.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#33](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#33)]  
  
##  <a name="ccombstr__appendbytes"></a>  CComBSTR::AppendBytes  
 Appends the specified number of bytes to [m_str](../vs140/CComBSTR--m_str.md) without conversion.  
  
```  
  
HRESULT AppendBytes(  
      const char* lpsz,  
      int nLen  
   ) throw( );  
  
```  
  
### Parameters  
 `lpsz`  
 [in] A pointer to an array of bytes to append.  
  
 `p`  
 [in] The number of bytes to append.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#34](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#34)]  
  
##  <a name="ccombstr__arraytobstr"></a>  CComBSTR::ArrayToBSTR  
 Frees any existing string held in the `CComBSTR` object, then creates a `BSTR` from the first character of each element in the safearray and attaches it to the `CComBSTR` object.  
  
```  
  
HRESULT ArrayToBSTR(  
      const SAFEARRAY*  pSrc   
   ) throw( );  
  
```  
  
### Parameters  
 `pSrc`  
 [in] The safearray containing the elements used to create the string.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
##  <a name="ccombstr__assignbstr"></a>  CComBSTR::AssignBSTR  
 Assigns a `BSTR` to [m_str](../vs140/CComBSTR--m_str.md).  
  
```  
  
HRESULT AssignBSTR(  
      const BSTR  bstrSrc  
   ) throw( );  
  
```  
  
### Parameters  
 `bstrSrc`  
 [in] A `BSTR` to assign to the current `CComBSTR` object.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
##  <a name="ccombstr__attach"></a>  CComBSTR::Attach  
 Attaches a `BSTR` to the `CComBSTR` object by setting the [m_str](../vs140/CComBSTR--m_str.md) member to *src*.  
  
```  
  
void Attach(  
      BSTR  src  
   ) throw( );  
  
```  
  
### Parameters  
 *src*  
 [in] The `BSTR` to attach to the object.  
  
### Remarks  
 Do not pass an ordinary wide-character string to this method. The compiler cannot catch the error and run time errors will occur.  
  
> [!NOTE]
>  This method will assert if `m_str` is non-                            **NULL**.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#35)]  
  
##  <a name="ccombstr__bstrtoarray"></a>  CComBSTR::BSTRToArray  
 Creates a zero-based one-dimensional safearray, where each element of the array is a character from the `CComBSTR` object.  
  
```  
  
HRESULT BSTRToArray(  
      LPSAFEARRAY*  ppArray   
   ) throw( );  
  
```  
  
### Parameters  
 `ppArray`  
 [out] The pointer to the safearray used to hold the results of the function.  
  
### Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
##  <a name="ccombstr__bytelength"></a>  CComBSTR::ByteLength  
 Returns the number of bytes in `m_str`, excluding the terminating null character.  
  
```  
  
unsigned int ByteLength( ) const throw( );  
  
```  
  
### Return Value  
 The length of the [m_str](../vs140/CComBSTR--m_str.md) member in bytes.  
  
### Remarks  
 Returns 0 if `m_str` is **NULL**.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#36](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#36)]  
  
##  <a name="ccombstr__ccombstr"></a>  CComBSTR::CComBSTR  
 The constructor. The default constructor sets the [m_str](../vs140/CComBSTR--m_str.md) member to **NULL**.  
  
```  
  
CComBSTR( ) throw( );   
   CComBSTR(  
      const CComBSTR&  src  
   );  
   CComBSTR(  
      REFGUID  guid  
   );  
   CComBSTR(  
      int  nSize  
   );  
   CComBSTR(  
      int  nSize,  
      LPCOLESTR  sz  
   );  
   CComBSTR(  
      int  nSize,  
      LPCSTR  sz  
   );  
   CComBSTR(  
      LPCOLESTR  pSrc  
   );  
   CComBSTR(  
      LPCSTR  pSrc  
   );  
   CComBSTR(  
                   CComBSTR&& src   
);  
  
```  
  
### Parameters  
 `nSize`  
 [in] The number of characters to copy from `sz` or the initial size in characters for the `CComBSTR`.  
  
 `sz`  
 [in] A string to copy. The Unicode version specifies an **LPCOLESTR**; the ANSI version specifies an `LPCSTR`.  
  
 `pSrc`  
 [in] A string to copy. The Unicode version specifies an **LPCOLESTR**; the ANSI version specifies an `LPCSTR`.  
  
 *src*  
 [in] A `CComBSTR` object.  
  
 `guid`  
 [in] A reference to a **GUID** structure.  
  
### Remarks  
 The copy constructor sets `m_str` to a copy of the `BSTR` member of *src*. The **REFGUID** constructor converts the **GUID** to a string using **StringFromGUID2** and stores the result.  
  
 The other constructors set `m_str` to a copy of the specified string. If you pass a value for `nSize`, then only `nSize` characters will be copied, followed by a terminating null character.  
  
 `CComBSTR` supports move semantics. You can use the move constructor (the constructor that takes an rvalue reference ( `&&`) to create a new object that uses the same underlying data as the old object you pass in as an argument, without the overhead of copying the object.  
  
 The destructor frees the string pointed to by `m_str`.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#37](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#37)]  
  
##  <a name="ccombstr___dtorccombstr"></a>  CComBSTR::~CComBSTR  
 The destructor.  
  
```  
  
~CComBSTR( );  
  
```  
  
### Remarks  
 The destructor frees the string pointed to by `m_str`.  
  
##  <a name="ccombstr__copy"></a>  CComBSTR::Copy  
 Allocates and returns a copy of `m_str`.  
  
```  
  
BSTR Copy( ) const throw();  
  
```  
  
### Return Value  
 A copy of the [m_str](../vs140/CComBSTR--m_str.md) member. If `m_str` is **NULL**, returns **NULL**.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#38](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#38)]  
  
##  <a name="ccombstr__copyto"></a>  CComBSTR::CopyTo  
 Allocates and returns a copy of [m_str](../vs140/CComBSTR--m_str.md) via the parameter.  
  
```  
  
HRESULT CopyTo(  
      BSTR*  pbstr   
   ) throw( );  
   HRESULT CopyTo(  
      VARIANT*  pvarDest   
   ) throw( );  
  
```  
  
### Parameters  
 *pbstr*  
 [out] The address of a `BSTR` in which to return the string allocated by this method.  
  
 `pvarDest`  
 [out] The address of a **VARIANT** in which to return the string allocated by this method.  
  
### Return Value  
 A standard `HRESULT` value indicating the success or failure of the copy.  
  
### Remarks  
 After calling this method, the **VARIANT** pointed to by `pvarDest` will be of type `VT_BSTR`.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#39](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#39)]  
  
##  <a name="ccombstr__detach"></a>  CComBSTR::Detach  
 Detaches [m_str](../vs140/CComBSTR--m_str.md) from the `CComBSTR` object and sets `m_str` to **NULL**.  
  
```  
  
BSTR Detach( ) throw( );  
  
```  
  
### Return Value  
 The `BSTR` associated with the `CComBSTR` object.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#40](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#40)]  
  
##  <a name="ccombstr__empty"></a>  CComBSTR::Empty  
 Frees the [m_str](../vs140/CComBSTR--m_str.md) member.  
  
```  
  
void Empty( ) throw( );  
  
```  
  
### Example  
 [!CODE [NVC_ATL_Utilities#41](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#41)]  
  
##  <a name="ccombstr__length"></a>  CComBSTR::Length  
 Returns the number of characters in `m_str`, excluding the terminating null character.  
  
```  
  
unsigned int Length( ) const throw( );  
  
```  
  
### Return Value  
 The length of the [m_str](../vs140/CComBSTR--m_str.md) member.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#42](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#42)]  
  
##  <a name="ccombstr__loadstring"></a>  CComBSTR::LoadString  
 Loads a string resource specified by `nID` and stores it in this object.  
  
```  
  
bool LoadString(  
      HINSTANCE  hInst,  
      UINT  nID  
   ) throw();  
   bool LoadString(  
      UINT  nID  
   ) throw();  
  
```  
  
### Parameters  
 See [LoadString](http://msdn.microsoft.com/library/windows/desktop/ms647486) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Return Value  
 Returns **true** if the string is successfully loaded; otherwise, returns **false**.  
  
### Remarks  
 The first function loads the resource from the module identified by you via the `hInst` parameter. The second function loads the resource from the resource module associated with the [CComModule](../vs140/CComModule-Class.md)-derived object used in this project.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#43](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#43)]  
  
##  <a name="ccombstr__m_str"></a>  CComBSTR::m_str  
 Contains the `BSTR` associated with the `CComBSTR` object.  
  
```  
  
BSTR m_str;  
  
```  
  
### Example  
 [!CODE [NVC_ATL_Utilities#49](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#49)]  
  
##  <a name="ccombstr__operator_bstr"></a>  CComBSTR::operator BSTR  
 Casts a `CComBSTR` object to a `BSTR`.  
  
```  
  
operator BSTR( ) const throw( );  
  
```  
  
### Remarks  
 Allows you to pass `CComBSTR` objects to functions that have **[in] BSTR** parameters.  
  
### Example  
 See the example for [CComBSTR::m_str](../vs140/CComBSTR--m_str.md).  
  
##  <a name="ccombstr__operator__not"></a>  CComBSTR::operator !  
 Checks whether `BSTR` string is NULL.  
  
```  
  
bool operator !( ) const throw( );  
  
```  
  
### Return Value  
 Returns **true** if the [m_str](../vs140/CComBSTR--m_str.md) member is **NULL**; otherwise,                         **false**.  
  
### Remarks  
 This operator only checks for a NULL value, not for an empty string.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#35)]  
  
##  <a name="ccombstr__operator__neq"></a>  CComBSTR::operator !=  
 Returns the logical opposite of [operator ==](../vs140/CComBSTR--operator-==.md).  
  
```  
  
bool operator!=(  
      const CComBSTR&  bstrSrc   
   ) const throw( );  
   bool operator!=(  
      LPCOLESTR  pszSrc   
   ) const;  
   bool operator!=(  
      LPCSTR  pszSrc   
   ) const;  
   bool operator!=(  
      int  nNull   
   ) const throw( );  
  
```  
  
### Parameters  
 `bstrSrc`  
 [in] A `CComBSTR` object.  
  
 `pszSrc`  
 [in] A zero-terminated string.  
  
 `nNull`  
 [in] Must be **NULL**.  
  
### Return Value  
 Returns **true** if the item being compared is not equal to the `CComBSTR` object; otherwise, returns **false**.  
  
### Remarks  
 `CComBSTR`s are compared textually in the context of the user's default locale. The final comparison operator just compares the contained string against **NULL**.  
  
##  <a name="ccombstr__operator__amp_"></a>  CComBSTR::operator &amp;  
 Returns the address of the `BSTR` stored in the [m_str](../vs140/CComBSTR--m_str.md) member.  
  
```  
BSTR* operator &( ) throw( );  
```  
  
### Remarks  
 `CComBstr operator &` has a special assertion associated with it to help identify memory leaks. The program will assert when the `m_str` member is initialized. This assertion was created to identify situations where a programmer uses the `& operator` to assign a new value to `m_str` member without freeing the first allocation of `m_str`. If `m_str` equals NULL, the program assumes that m_str wasn't allocated yet. In this case, the program will not assert.  
  
 This assertion is not enabled by default. Define `ATL_CCOMBSTR_ADDRESS_OF_ASSERT` to enable this assertion.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#46](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#46)]  
  
 [!CODE [NVC_ATL_Utilities#47](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#47)]  
  
##  <a name="ccombstr__operator__add_eq"></a>  CComBSTR::operator +=  
 Appends a string to the `CComBSTR` object.  
  
```  
  
CComBSTR& operator +=(  
      const CComBSTR&  bstrSrc  
   );  
   CComBSTR& operator +=(  
      const LPCOLESTR  pszSrc  
   );  
  
```  
  
### Parameters  
 `bstrSrc`  
 [in] A `CComBSTR` object to append.  
  
 `pszSrc`  
 [in] A zero-terminated string to append.  
  
### Remarks  
 `CComBSTR`s are compared textually in the context of the user's default locale. The **LPCOLESTR** comparison is done using `memcmp` on the raw data in each string. The `LPCSTR` comparison is carried out in the same way once a temporary Unicode copy of `pszSrc` has been created. The final comparison operator just compares the contained string against **NULL**.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#48](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#48)]  
  
##  <a name="ccombstr__operator__lt_"></a>  CComBSTR::operator &lt;  
 Compares a `CComBSTR` with a string.  
  
```  
  
bool operator <(  
      const CComBSTR&  bstrSrc   
   ) const throw( );  
   bool operator <(  
      LPCOLESTR  pszSrc   
   ) const throw( );  
   bool operator <(  
      LPCSTR  pszSrc   
   ) const throw( );  
  
```  
  
### Return Value  
 Returns **true** if the item being compared is less than the `CComBSTR` object; otherwise, returns **false**.  
  
### Remarks  
 The comparison is performed using the user's default locale.  
  
##  <a name="ccombstr__operator__eq"></a>  CComBSTR::operator =  
 Sets the [m_str](../vs140/CComBSTR--m_str.md) member to a copy of `pSrc` or to a copy of the `BSTR` member of *src*.  
  
```  
  
CComBSTR& operator =(  
      const CComBSTR&  src  
   );  
   CComBSTR& operator =(  
      LPCOLESTR  pSrc  
   );  
   CComBSTR& operator =(  
      LPCSTR  pSrc  
   );  
  
```  
  
### Remarks  
 The `pSrc` parameter specifies either an **LPCOLESTR** for Unicode versions or `LPCSTR` for ANSI versions.  
  
### Example  
 See the example for [CComBSTR::Copy](../vs140/CComBSTR--Copy.md).  
  
##  <a name="ccombstr__operator__eq_eq"></a>  CComBSTR::operator ==  
 Compares a `CComBSTR` with a string. `CComBSTR`s are compared textually in the context of the user's default locale.  
  
```  
  
bool operator ==(  
      const CComBSTR&  bstrSrc   
   ) const throw( );  
   bool operator ==(  
      LPCOLESTR  pszSrc   
   ) const;  
   bool operator ==(  
      LPCSTR  pszSrc   
   ) const;  
   bool operator ==(  
      int  nNull   
   ) const throw( );  
  
```  
  
### Parameters  
 `bstrSrc`  
 [in] A `CComBSTR` object.  
  
 `pszSrc`  
 [in] A zero-terminated string.  
  
 `nNull`  
 [in] Must be **NULL**.  
  
### Return Value  
 Returns **true** if the item being compared is equal to the `CComBSTR` object; otherwise, returns **false**.  
  
### Remarks  
 The final comparison operator just compares the contained string against **NULL**.  
  
##  <a name="ccombstr__operator__gt_"></a>  CComBSTR::operator &gt;  
 Compares a `CComBSTR` with a string.  
  
```  
  
bool operator >(  
      const CComBSTR&  bstrSrc   
   ) const throw( );  
  
```  
  
### Return Value  
 Returns **true** if the item being compared is greater than the `CComBSTR` object; otherwise, returns **false**.  
  
### Remarks  
 The comparison is performed using the user's default locale.  
  
##  <a name="ccombstr__readfromstream"></a>  CComBSTR::ReadFromStream  
 Sets the [m_str](../vs140/CComBSTR--m_str.md) member to the `BSTR` contained in the specified stream.  
  
```  
  
HRESULT ReadFromStream(  
      IStream*  pStream  
   ) throw( );  
  
```  
  
### Parameters  
 `pStream`  
 [in] A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface on the stream containing the data.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 **ReadToStream** requires the contents of the stream at the current position to be compatible with the data format written out by a call to [WriteToStream](../vs140/CComBSTR--WriteToStream.md).  
  
### Example  
 [!CODE [NVC_ATL_Utilities#44](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#44)]  
  
##  <a name="ccombstr__tolower"></a>  CComBSTR::ToLower  
 Converts the contained string to lowercase.  
  
```  
  
HRESULT ToLower( ) throw( );  
  
```  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 See **CharLowerBuff** for more information on how the conversion is performed.  
  
##  <a name="ccombstr__toupper"></a>  CComBSTR::ToUpper  
 Converts the contained string to uppercase.  
  
```  
  
HRESULT ToUpper( ) throw( );  
  
```  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 See **CharUpperBuff** for more information on how the conversion is performed.  
  
##  <a name="ccombstr__writetostream"></a>  CComBSTR::WriteToStream  
 Saves the [m_str](../vs140/CComBSTR--m_str.md) member to a stream.  
  
```  
  
HRESULT WriteToStream(  
      IStream*  pStream  
   ) throw( );  
  
```  
  
### Parameters  
 `pStream`  
 [in] A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface on a stream.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 You can recreate a BSTR from the contents of the stream using the [ReadFromStream](../vs140/CComBSTR--ReadFromStream.md) function.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#45](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#45)]  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md)