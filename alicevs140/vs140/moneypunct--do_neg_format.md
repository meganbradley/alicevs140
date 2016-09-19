---
title: "moneypunct::do_neg_format"
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
ms.assetid: a248e839-cc88-489b-860f-1fd03e99246d
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# moneypunct::do_neg_format
A protected virtual member function that is called to return a locale-specific rule for formatting outputs with negative amounts.  
  
## Syntax  
  
```  
virtual pattern do_neg_format( ) const;  
```  
  
## Return Value  
 The protected virtual member function returns a locale-specific rule for determining how to generate a monetary output field for a negative amount. Each of the four elements of **pattern::field** can have the values:  
  
-   **none** to match zero or more spaces or generate nothing.  
  
-   **sign** to match or generate a positive or negative sign.  
  
-   **space** to match zero or more spaces or generate a space.  
  
-   **symbol** to match or generate a currency symbol.  
  
-   **value** to match or generate a monetary value.  
  
 Components of a monetary output field are generated and components of a monetary input field are matched in the order in which these elements appear in **pattern::field**. Each of the values **sign**, **symbol**, **value**, and either **none** or **space** must appear exactly once. The value **none** must not appear first. The value space **must** not appear first or last. If **Intl** is true, the order is **symbol**, **sign**, **none**, then **value**.  
  
 The template version of `moneypunct`<**CharType**, **Intl**> returns `{`**money_base::symbol**, **money_base::sign**, **money_base::value**, **money_base::none**`}`.  
  
## Example  
 See the example for [neg_format](../vs140/moneypunct--neg_format.md), where the virtual member function is called by `neg_format`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)