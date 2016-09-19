---
title: "COleCurrency::Format"
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
ms.assetid: 3807eb9a-8785-4993-8e5a-09ac59793eda
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::Format
Call this member function to create a formatted representation of the currency value.  
  
## Syntax  
  
```  
  
      CString Format(   
   DWORD dwFlags = 0,   
   LCID lcid = LANG_USER_DEFAULT    
) const;  
```  
  
#### Parameters  
 `dwFlags`  
 Indicates flags for locale settings. Only the following flag is relevant to currency:  
  
-   **LOCALE_NOUSEROVERRIDE** Use the system default locale settings, rather than custom user settings.  
  
 `lcid`  
 Indicates locale ID to use for the conversion.  
  
## Return Value  
 A `CString` that contains the formatted currency value.  
  
## Remarks  
 It formats the value using the local language specifications (locale IDs). A currency symbol is not included in the value returned. If the status of this **COleCurrency** object is null, the return value is an empty string. If the status is invalid, the return string is specified by the string resource **IDS_INVALID_CURRENCY**.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#11)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::ParseCurrency](../vs140/COleCurrency--ParseCurrency.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)