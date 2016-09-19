---
title: "How to: Use Regular Expressions to Rearrange Data (C++-CLI)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: How to: Use Regular Expressions to Rearrange Data (C++/CLI)
ms.assetid: 5f91e777-9471-424e-ba75-dca3d1b49e42
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Regular Expressions to Rearrange Data (C++-CLI)
The following code example demonstrates how the .NET Framework regular expression support can be used to rearrange, or reformat data. The following code example uses the <xref:System.Text.RegularExpressions.Regex?qualifyHint=False> and <xref:System.Text.RegularExpressions.Match?qualifyHint=False> classes to extract first and last names from a string and then display these name elements in reverse order.  
  
 The <xref:System.Text.RegularExpressions.Regex?qualifyHint=False> class is used to construct a regular expression that describes the current format of the data. The two names are assumed to be separated by a comma and can use any amount of white-space around the comma. The <xref:System.Text.RegularExpressions.Match?qualifyHint=False> method is then used to analyze each string. If successful, first and last names are retrieved from the <xref:System.Text.RegularExpressions.Match?qualifyHint=False> object and displayed.  
  
## Example  
  
```  
// regex_reorder.cpp  
// compile with: /clr  
#using <System.dll>  
using namespace System;  
using namespace Text::RegularExpressions;  
  
int main()  
{  
   array<String^>^ name =   
   {  
      "Abolrous, Sam",   
      "Berg,Matt",   
      "Berry , Jo",  
      "www.contoso.com"  
   };  
  
   Regex^ reg = gcnew Regex("(?<last>\\w*)\\s*,\\s*(?<first>\\w*)");  
  
   for ( int i=0; i < name->Length; i++ )  
   {  
      Console::Write( "{0,-20}", name[i] );  
      Match^ m = reg->Match( name[i] );  
      if ( m->Success )  
      {  
         String^ first = m->Groups["first"]->Value;  
         String^ last = m->Groups["last"]->Value;  
         Console::WriteLine("{0} {1}", first, last);  
      }  
      else  
         Console::WriteLine("(invalid)");  
   }  
   return 0;  
}  
```  
  
## See Also  
 [.NET Framework Regular Expressions](assetId:///521b3f6d-f869-42e1-93e5-158c54a6895d)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)