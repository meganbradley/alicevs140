---
title: "Formatting Numeric Results Table (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 120ba537-4448-4c62-8676-7a8fdd98f496
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Formatting Numeric Results Table (C# Reference)
You can format numeric results by using the <xref:System.String.Format?qualifyHint=True> method, or through the <xref:System.Console.Write?qualifyHint=True> or <xref:System.Console.WriteLine?qualifyHint=True> method, which calls `String.Format`. The format is specified by using format strings. The following table contains the supported standard format strings. The format string takes the following form: `Axx`, where `A` is the format specifier and `xx` is the precision specifier. The format specifier controls the type of formatting applied to the numeric value, and the precision specifier controls the number of significant digits or decimal places of the formatted output. The value of the precision specifier ranges from 0 to 99.  
  
 For more information about standard and custom formatting strings, see [Formatting Types](assetId:///0d1364da-5b30-4d42-8e6b-03378343343f). For more information about the `String.Format` method, see <xref:System.String.Format?qualifyHint=True>.  
  
|Format Specifier|Description|Examples|Output|  
|----------------------|-----------------|--------------|------------|  
|C or c|Currency|Console.Write("{0:C}", 2.5);<br /><br /> Console.Write("{0:C}", -2.5);|$2.50<br /><br /> ($2.50)|  
|D or d|Decimal|Console.Write("{0:D5}", 25);|00025|  
|E or e|Scientific|Console.Write("{0:E}", 250000);|2.500000E+005|  
|F or f|Fixed-point|Console.Write("{0:F2}", 25);<br /><br /> Console.Write("{0:F0}", 25);|25.00<br /><br /> 25|  
|G or g|General|Console.Write("{0:G}", 2.5);|2.5|  
|N or n|Number|Console.Write("{0:N}", 2500000);|2,500,000.00|  
|X or x|Hexadecimal|Console.Write("{0:X}", 250);<br /><br /> Console.Write("{0:X}", 0xffff);|FA<br /><br /> FFFF|  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Standard Numeric Format Strings](assetId:///580e57eb-ac47-4ffd-bccd-3a1637c2f467)   
 [Reference Tables for Types](../vs140/Reference-Tables-for-Types--C#-Reference-.md)   
 [string](../Topic/string%20\(C%23%20Reference\).md)