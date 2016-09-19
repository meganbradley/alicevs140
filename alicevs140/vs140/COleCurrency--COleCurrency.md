---
title: "COleCurrency::COleCurrency"
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
ms.assetid: c3ad2bf0-54bd-4d05-927f-4fa47e026ae9
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::COleCurrency
Constructs a **COleCurrency** object.  
  
## Syntax  
  
```  
  
      COleCurrency( );  
COleCurrency(  
   CURRENCY cySrc   
);  
COleCurrency(  
   const COleCurrency& curSrc   
);  
COleCurrency(  
   const VARIANT& varSrc   
);  
COleCurrency(  
   long nUnits,  
   long nFractionalUnits   
);  
```  
  
#### Parameters  
 `cySrc`  
 A **CURRENCY** value to be copied into the new **COleCurrency** object.  
  
 `curSrc`  
 An existing **COleCurrency** object to be copied into the new **COleCurrency** object.  
  
 *varSrc*  
 An existing **VARIANT** data structure (possibly a `COleVariant` object) to be converted to a currency value (`VT_CY`) and copied into the new **COleCurrency** object.  
  
 `nUnits`, `nFractionalUnits`  
 Indicate the units and fractional part (in 1/10,000's) of the value to be copied into the new **COleCurrency** object.  
  
## Remarks  
 All of these constructors create new **COleCurrency** objects initialized to the specified value. A brief description of each of these constructors follows. Unless otherwise noted, the status of the new **COleCurrency** item is set to valid.  
  
-   `COleCurrency(` **)** Constructs a **COleCurrency** object initialized to 0 (zero).  
  
-   `COleCurrency(` `cySrc` **)** Constructs a **COleCurrency** object from a [CURRENCY](assetId:///5e81273c-7289-45c7-93c0-32c1553f708e) value.  
  
-   `COleCurrency(` `curSrc` **)** Constructs a **COleCurrency** object from an existing **COleCurrency** object. The new object has the same status as the source object.  
  
-   `COleCurrency(` *varSrc* **)** Constructs a **COleCurrency** object. Attempts to convert a [VARIANT](assetId:///e305240e-9e11-4006-98cc-26f4932d2118) structure or `COleVariant` object to a currency (`VT_CY`) value. If this conversion is successful, the converted value is copied into the new **COleCurrency** object. If it is not, the value of the **COleCurrency** object is set to zero (0) and its status to invalid.  
  
-   `COleCurrency(` `nUnits`**,** `nFractionalUnits` **)** Constructs a **COleCurrency** object from the specified numerical components. If the absolute value of the fractional part is greater than 10,000, the appropriate adjustment is made to the units. Note that the units and fractional part are specified by signed long values.  
  
 For more information, see the [CURRENCY](assetId:///5e81273c-7289-45c7-93c0-32c1553f708e) and [VARIANT](assetId:///e305240e-9e11-4006-98cc-26f4932d2118) entries in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following examples show the effects of the zero-parameter and two-parameter constructors:  
  
 [!CODE [NVC_MFCOleContainer#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#10)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::SetCurrency](../vs140/COleCurrency--SetCurrency.md)   
 [COleCurrency::operator =](../vs140/COleCurrency--operator-=.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)   
 [COleCurrency::m_cur](../vs140/COleCurrency--m_cur.md)   
 [COleCurrency::m_status](../vs140/COleCurrency--m_status.md)