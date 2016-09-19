---
title: "How to: Parse Strings Using Regular Expressions (C++-CLI)"
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
H1: How to: Parse Strings Using Regular Expressions (C++/CLI)
ms.assetid: 5b0c7ca3-9bba-4389-a45c-6d373cff91b0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Parse Strings Using Regular Expressions (C++-CLI)
The following code example demonstrates simple string parsing using the <xref:System.Text.RegularExpressions.Regex?qualifyHint=False> class in the <xref:System.Text.RegularExpressions?qualifyHint=True> namespace. A string containing multiple types of word delineators is constructed. The string is then parsed using the <xref:System.Text.RegularExpressions.Regex?qualifyHint=False> class in conjunction with the <xref:System.Text.RegularExpressions.Match?qualifyHint=False> class. Then, each word in the sentence is displayed separately.  
  
## Example  
  
```  
// regex_parse.cpp  
// compile with: /clr  
#using <system.dll>  
  
using namespace System;  
using namespace System::Text::RegularExpressions;  
  
int main( )  
{  
   int words = 0;  
   String^ pattern = "[a-zA-Z]*";  
   Console::WriteLine( "pattern : '{0}'", pattern );  
   Regex^ regex = gcnew Regex( pattern );  
  
   String^ line = "one\ttwo three:four,five six  seven";     
   Console::WriteLine( "text : '{0}'", line );  
   for( Match^ match = regex->Match( line );   
        match->Success; match = match->NextMatch( ) )   
   {  
      if( match->Value->Length > 0 )  
      {  
         words++;  
         Console::WriteLine( "{0}", match->Value );  
      }  
   }  
   Console::WriteLine( "Number of Words : {0}", words );  
  
   return 0;  
}  
```  
  
## See Also  
 [.NET Framework Regular Expressions](assetId:///521b3f6d-f869-42e1-93e5-158c54a6895d)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)