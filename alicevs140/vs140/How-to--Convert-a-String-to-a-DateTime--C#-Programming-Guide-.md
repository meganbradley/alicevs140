---
title: "How to: Convert a String to a DateTime (C# Programming Guide)"
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
ms.assetid: 88abef11-3a06-4b49-8dd2-61ed0e876fc3
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert a String to a DateTime (C# Programming Guide)
It is common for programs to enable users to enter dates as string values. To convert a string-based date to a <xref:System.DateTime?qualifyHint=True> object, you can use the <xref:System.Convert.ToDateTime(System.String)?qualifyHint=True> method or the <xref:System.DateTime.Parse(System.String)?qualifyHint=True> static method, as shown in the following example.  
  
 **Culture**.  Different cultures in the world write date strings in different ways.  For example, in the US 01/20/2008 is January 20th, 2008.  In France this will throw an InvalidFormatException. This is because France reads date-times as Day/Month/Year, and in the US it is Month/Day/Year.  
  
 Consequently, a string like 20/01/2008 will parse to January 20th, 2008 in France, and then throw an InvalidFormatException in the US.  
  
 To determine your current culture settings, you can use System.Globalization.CultureInfo.CurrentCulture.  
  
 See the example below for a simple example of converting a string to dateTime.  
  
 For more examples of date strings, see <xref:System.Convert.ToDateTime(System.String)?qualifyHint=True>.  
  
```c#  
string dateTime = "01/08/2008 14:50:50.42";  
            DateTime dt = Convert.ToDateTime(dateTime);  
            Console.WriteLine("Year: {0}, Month: {1}, Day: {2}, Hour: {3}, Minute: {4}, Second: {5}, Millisecond: {6}",  
                              dt.Year, dt.Month, dt.Day, dt.Hour, dt.Minute, dt.Second, dt.Millisecond);  
            // Specify exactly how to interpret the string.  
            IFormatProvider culture = new System.Globalization.CultureInfo("fr-FR", true);  
  
            // Alternate choice: If the string has been input by an end user, you might    
            // want to format it according to the current culture:   
            // IFormatProvider culture = System.Threading.Thread.CurrentThread.CurrentCulture;  
            DateTime dt2 = DateTime.Parse(dateTime, culture, System.Globalization.DateTimeStyles.AssumeLocal);  
            Console.WriteLine("Year: {0}, Month: {1}, Day: {2}, Hour: {3}, Minute: {4}, Second: {5}, Millisecond: {6}",  
                              dt2.Year, dt2.Month, dt2.Day, dt2.Hour, dt2.Minute, dt2.Second, dt2.Millisecond  
/* Output (assuming first culture is en-US and second is fr-FR):  
    Year: 2008, Month: 1, Day: 8, Hour: 14, Minute: 50, Second: 50, Millisecond: 420  
Year: 2008, Month: 8, Day: 1, Hour: 14, Minute: 50, Second: 50, Millisecond: 420  
Press any key to continue . . .  
 */  
```  
  
## Example  
 [!CODE [csProgGuideStrings#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStrings#13)]  
  
## See Also  
 [Strings Overview (C# Programming Guide)](../Topic/Strings%20\(C%23%20Programming%20Guide\).md)