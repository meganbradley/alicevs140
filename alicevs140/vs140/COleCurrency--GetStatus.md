---
title: "COleCurrency::GetStatus"
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
ms.assetid: 3c0c8750-a598-4c4b-9e8b-28cf72dcb1ff
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::GetStatus
Call this member function to get the status (validity) of a given **COleCurrency** object.  
  
## Syntax  
  
```  
  
CurrencyStatus GetStatus( ) const;  
  
```  
  
## Return Value  
 Returns the status of this **COleCurrency** value.  
  
## Remarks  
 The return value is defined by the `CurrencyStatus` enumerated type that is defined within the **COleCurrency** class.  
  
 `enum CurrencyStatus{`  
  
 `valid = 0,`  
  
 `invalid = 1,`  
  
 `null = 2,`  
  
 `};`  
  
 For a brief description of these status values, see the following list:  
  
-   **COleCurrency::valid** Indicates that this **COleCurrency** object is valid.  
  
-   **COleCurrency::invalid** Indicates that this **COleCurrency** object is invalid; that is, its value may be incorrect.  
  
-   **COleCurrency::null** Indicates that this **COleCurrency** object is null, that is, that no value has been supplied for this object. (This is "null" in the database sense of "having no value," as opposed to the C++ **NULL**.)  
  
 The status of a **COleCurrency** object is invalid in the following cases:  
  
-   If its value is set from a **VARIANT** or `COleVariant` value that could not be converted to a currency value.  
  
-   If this object has experienced an overflow or underflow during an arithmetic assignment operation, for example `+=` or **\*=**.  
  
-   If an invalid value was assigned to this object.  
  
-   If the status of this object was explicitly set to invalid using [SetStatus](../vs140/COleCurrency--SetStatus.md).  
  
 For more information on operations that may set the status to invalid, see the following member functions:  
  
-   [COleCurrency](../vs140/COleCurrency--COleCurrency.md)  
  
-   [operator =](../vs140/COleCurrency--operator-=.md)  
  
-   [operator +, -](../vs140/COleCurrency--operator-----.md)  
  
-   [operator +=, -=](../vs140/COleCurrency--operator--=---=.md)  
  
-   [operator *, /](../vs140/COleCurrency--operator-----.md)  
  
-   [operator *=, /=](../vs140/COleCurrency--operator--=---=.md)  
  
## Example  
 [!CODE [NVC_MFCOleContainer#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#12)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::SetStatus](../vs140/COleCurrency--SetStatus.md)   
 [COleCurrency::m_status](../vs140/COleCurrency--m_status.md)