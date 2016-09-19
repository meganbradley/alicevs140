---
title: "COleVariant::COleVariant"
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
ms.assetid: 4aacf985-71fa-475f-91f0-7cf44d4cbe63
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleVariant::COleVariant
Constructs a `COleVariant` object.  
  
## Syntax  
  
```  
  
      COleVariant( );   
COleVariant(  
   const VARIANT& varSrc   
);  
COleVariant(  
   const COleVariant& varSrc   
);  
COleVariant(  
   LPCVARIANT pSrc   
);  
COleVariant(  
   LPCTSTR lpszSrc   
);  
COleVariant(  
   LPCTSTR lpszSrc,  
   VARTYPE vtSrc   
);  
COleVariant(  
   CString& strSrc   
);  
COleVariant(  
   BYTE nSrc   
);  
COleVariant(  
   short nSrc,  
   VARTYPE vtSrc = VT_I2   
);  
COleVariant(  
   long lSrc,  
   VARTYPE vtSrc = VT_I4   
);  
COleVariant(  
   const COleCurrency& curSrc   
);  
COleVariant(  
   float fltSrc   
);  
COleVariant(  
   double dblSrc   
);  
COleVariant(  
   const COleDateTime& timeSrc   
);  
COleVariant(  
   const CByteArray& arrSrc   
);  
COleVariant(  
   const CLongBinary& lbSrc   
);  
COleVariant(  
   LPCITEMIDLIST pidl  
);  
```  
  
#### Parameters  
 *varSrc*  
 An existing `COleVariant` or **VARIANT** object to be copied into the new `COleVariant` object.  
  
 `pSrc`  
 A pointer to a **VARIANT** object that will be copied into the new `COleVariant` object.  
  
 `lpszSrc`  
 A null-terminated string to be copied into the new `COleVariant` object.  
  
 `vtSrc`  
 The `VARTYPE` for the new `COleVariant` object.  
  
 `strSrc`  
 A [CString](../vs140/CStringT-Class.md) object to be copied into the new `COleVariant` object.  
  
 `nSrc`, `lSrc`  
 A numerical value to be copied into the new `COleVariant` object.  
  
 `vtSrc`  
 The `VARTYPE` for the new `COleVariant` object.  
  
 `curSrc`  
 A [COleCurrency](../vs140/COleCurrency-Class.md) object to be copied into the new `COleVariant` object.  
  
 `fltSrc`, `dblSrc`  
 A numerical value to be copied into the new `COleVariant` object.  
  
 `timeSrc`  
 A [COleDateTime](../vs140/COleDateTime-Class.md) object to be copied into the new `COleVariant` object.  
  
 `arrSrc`  
 A [CByteArray](../vs140/CByteArray-Class.md) object to be copied into the new `COleVariant` object.  
  
 `lbSrc`  
 A [CLongBinary](../vs140/CLongBinary-Class.md) object to be copied into the new `COleVariant` object.  
  
 `pidl`  
 A pointer to a [ITEMIDLIST](http://msdn.microsoft.com/library/windows/desktop/bb773321) structure to be copied into the new `COleVariant` object.  
  
## Remarks  
 All these constructors create new `COleVariant` objects initialized to the specified value. A brief description of each of these constructors follows.  
  
-   **COleVariant( )** Creates an empty `COleVariant` object, `VT_EMPTY`.  
  
-   **COleVariant(**  *varSrc*  **)** Copies an existing **VARIANT** or `COleVariant` object. The variant type is retained.  
  
-   **COleVariant(**  `pSrc`  **)** Copies an existing **VARIANT** or `COleVariant` object. The variant type is retained.  
  
-   **COleVariant(**  `lpszSrc`  **)** Copies a string into the new object, `VT_BSTR` (UNICODE).  
  
-   **COleVariant(**  `lpszSrc` **,**  `vtSrc`  **)** Copies a string into the new object. The parameter `vtSrc` must be `VT_BSTR` (UNICODE) or `VT_BSTRT` (ANSI).  
  
-   **COleVariant(**  `strSrc`  **)** Copies a string into the new object, **VT_BSTR** (UNICODE).  
  
-   **COleVariant(**  `nSrc`  **)** Copies an 8-bit integer into the new object, `VT_UI1`.  
  
-   **COleVariant(**  `nSrc` **,**  `vtSrc`  **)** Copies a 16-bit integer (or Boolean value) into the new object. The parameter `vtSrc` must be `VT_I2` or `VT_BOOL`.  
  
-   **COleVariant(**  `lSrc` **,**  `vtSrc`  **)** Copies a 32-bit integer (or `SCODE` value) into the new object. The parameter `vtSrc` must be `VT_I4`, `VT_ERROR`, or `VT_BOOL`.  
  
-   **COleVariant(**  `curSrc`  **)** Copies a **COleCurrency** value into the new object, `VT_CY`.  
  
-   **COleVariant(**  `fltSrc`  **)** Copies a 32-bit floating-point value into the new object, `VT_R4`.  
  
-   **COleVariant(**  `dblSrc`  **)** Copies a 64-bit floating-point value into the new object, `VT_R8`.  
  
-   **COleVariant(**  `timeSrc`  **)** Copies a `COleDateTime` value into the new object, `VT_DATE`.  
  
-   **COleVariant(**  `arrSrc`  **)** Copies a `CByteArray` object into the new object, `VT_EMPTY`.  
  
-   **COleVariant(**  `lbSrc`  **)** Copies a `CLongBinary` object into the new object, `VT_EMPTY`.  
  
 For more information on `SCODE`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleVariant Class](../vs140/COleVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleVariant::operator =](../vs140/COleVariant--operator-=.md)   
 [CStringT Class](../vs140/CStringT-Class.md)   
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [COleDateTime Class](../vs140/COleDateTime-Class.md)