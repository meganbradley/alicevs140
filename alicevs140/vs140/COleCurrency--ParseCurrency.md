---
title: "COleCurrency::ParseCurrency"
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
ms.assetid: 92a06ce9-0186-4286-a3c4-179021833fc6
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::ParseCurrency
Call this member function to parse a string to read a currency value.  
  
## Syntax  
  
```  
  
      BOOL ParseCurrency(  
   LPCTSTR lpszCurrency,  
   DWORD dwFlags = 0,  
   LCID lcid = LANG_USER_DEFAULT   
);  
throw(  
   CMemoryException*   
);  
throw(  
   COleException*   
);  
```  
  
#### Parameters  
 *lpszCurrency*  
 A pointer to the null-terminated string which is to be parsed.  
  
 `dwFlags`  
 Indicates flags for locale settings, possibly the following flag:  
  
-   **LOCALE_NOUSEROVERRIDE** Use the system default locale settings, rather than custom user settings.  
  
 `lcid`  
 Indicates locale ID to use for the conversion.  
  
## Return Value  
 Nonzero if the string was successfully converted to a currency value, otherwise 0.  
  
## Remarks  
 It uses local language specifications (locale IDs) for the meaning of nonnumeric characters in the source string.  
  
 For a discussion of locale ID values, see [Supporting Multiple Languages](assetId:///47dc5add-232c-4268-b977-43e12da81ede).  
  
 If the string was successfully converted to a currency value, the value of this **COleCurrency** object is set to that value and its status to valid.  
  
 If the string could not be converted to a currency value or if there was a numerical overflow, the status of this **COleCurrency** object is invalid.  
  
 If the string conversion failed due to memory allocation errors, this function throws a [CMemoryException](../vs140/CMemoryException-Class.md). In any other error state, this function throws a [COleException](../vs140/COleException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#13)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::Format](../vs140/COleCurrency--Format.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)