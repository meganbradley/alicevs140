---
title: "COleCurrency::operator ="
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
ms.assetid: 11b906ce-0840-49f5-9ba2-2846fb257ade
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::operator =
These overloaded assignment operators copy the source currency value into this **COleCurrency** object.  
  
## Syntax  
  
```  
  
      const COleCurrency& operator =(  
   CURRENCY cySrc   
);  
const COleCurrency& operator =(  
   const COleCurrency& curSrc   
);  
const COleCurrency& operator =(  
   const VARIANT& varSrc   
);  
```  
  
## Remarks  
 A brief description of each operator follows:  
  
-   **operator =(**  `cySrc`  **)** The `CURRENCY` value is copied into the **COleCurrency** object and its status is set to valid.  
  
-   **operator =(**  `curSrc`  **)** The value and status of the operand, an existing **COleCurrency** object are copied into this **COleCurrency** object.  
  
-   **operator =(**  *varSrc*  **)** If the conversion of the `VARIANT` value (or [COleVariant](../vs140/COleVariant-Class.md) object) to a currency (`VT_CY`) is successful, the converted value is copied into this **COleCurrency** object and its status is set to valid. If the conversion is not successful, the value of the **COleCurrency** object is set to 0 and its status to invalid.  
  
 For more information, see the [CURRENCY](assetId:///5e81273c-7289-45c7-93c0-32c1553f708e) and [VARIANT](assetId:///e305240e-9e11-4006-98cc-26f4932d2118) entries in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCOleContainer#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#15)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::COleCurrency](../vs140/COleCurrency--COleCurrency.md)   
 [COleCurrency::SetCurrency](../vs140/COleCurrency--SetCurrency.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)