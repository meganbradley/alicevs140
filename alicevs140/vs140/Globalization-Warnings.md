---
title: "Globalization Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8d12d41-14bf-4b43-af24-168312d7c390
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Globalization Warnings
Globalization warnings support world-ready libraries and applications.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1300: Specify MessageBoxOptions](../Topic/CA1300:%20Specify%20MessageBoxOptions.md)|To correctly display a message box for cultures that use a right-to-left reading order, the RightAlign and RtlReading members of the MessageBoxOptions enumeration must be passed to the Show method.|  
|[CA1301: Avoid duplicate accelerators](../Topic/CA1301:%20Avoid%20duplicate%20accelerators.md)|An access key, also known as an accelerator, enables keyboard access to a control by using the ALT key. When multiple controls have duplicate access keys, the behavior of the access key is not well defined.|  
|[CA1302: Do not hardcode locale specific strings](../Topic/CA1302:%20Do%20not%20hardcode%20locale%20specific%20strings.md)|The System.Environment.SpecialFolder enumeration contains members that refer to special system folders. The locations of these folders can have different values on different operating systems; the user can change some of the locations; and the locations are localized. The Environment.GetFolderPath method returns the locations that are associated with the Environment.SpecialFolder enumeration, localized and appropriate for the currently running computer.|  
|[CA1303: Do not pass literals as localized parameters](../Topic/CA1303:%20Do%20not%20pass%20literals%20as%20localized%20parameters.md)|An externally visible method passes a string literal as a parameter to a constructor or method in the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] class library, and that string should be localizable.|  
|[CA1304: Specify CultureInfo](../vs140/CA1304--Specify-CultureInfo.md)|A method or constructor calls a member that has an overload that accepts a System.Globalization.CultureInfo parameter, and the method or constructor does not call the overload that takes the CultureInfo parameter. When a CultureInfo or System.IFormatProvider object is not supplied, the default value that is supplied by the overloaded member might not have the effect that you want in all locales.|  
|[CA1305: Specify IFormatProvider](../Topic/CA1305:%20Specify%20IFormatProvider.md)|A method or constructor calls one or more members that have overloads that accept a System.IFormatProvider parameter, and the method or constructor does not call the overload that takes the IFormatProvider parameter. When a System.Globalization.CultureInfo or IFormatProvider object is not supplied, the default value that is supplied by the overloaded member might not have the effect that you want in all locales.|  
|[CA1306: Set locale for data types](../vs140/CA1306--Set-locale-for-data-types.md)|The locale determines culture-specific presentation elements for data, such as formatting that is used for numeric values, currency symbols, and sort order. When you create a DataTable or DataSet, you should explicitly set the locale.|  
|[CA1307: Specify StringComparison](../vs140/CA1307--Specify-StringComparison.md)|A string comparison operation uses a method overload that does not set a StringComparison parameter.|  
|[CA1308: Normalize strings to uppercase](../vs140/CA1308--Normalize-strings-to-uppercase.md)|Strings should be normalized to uppercase. A small group of characters cannot make a round trip when they are converted to lowercase.|  
|[CA1309: Use ordinal StringComparison](../Topic/CA1309:%20Use%20ordinal%20StringComparison.md)|A string comparison operation that is nonlinguistic does not set the StringComparison parameter to either Ordinal or OrdinalIgnoreCase. By explicitly setting the parameter to either StringComparison.Ordinal or StringComparison.OrdinalIgnoreCase, your code often gains speed, becomes more correct, and becomes more reliable.|  
|[CA2101: Specify marshaling for P/Invoke string arguments](../vs140/CA2101--Specify-marshaling-for-P-Invoke-string-arguments.md)|A platform invoke member allows for partially trusted callers, has a string parameter, and does not explicitly marshal the string. This can cause a potential security vulnerability.|