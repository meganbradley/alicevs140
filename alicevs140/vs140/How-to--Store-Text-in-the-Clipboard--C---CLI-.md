---
title: "How to: Store Text in the Clipboard (C++-CLI)"
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
H1: How to: Store Text in the Clipboard (C++/CLI)
ms.assetid: 9996023f-b700-47ad-8ad9-1ba201eaa5a6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Store Text in the Clipboard (C++-CLI)
The following code example uses the <xref:System.Windows.Forms.Clipboard?qualifyHint=False> object defined in the <xref:System.Windows.Forms?qualifyHint=False> namespace to store a string. This object provides two member functions: <xref:System.Windows.Forms.Clipboard.SetDataObject?qualifyHint=False> and <xref:System.Windows.Forms.Clipboard.GetDataObject?qualifyHint=False>. Data is stored in the Clipboard by sending any object derived from <xref:System.Object?qualifyHint=False> to <xref:System.Windows.Forms.Clipboard.SetDataObject?qualifyHint=False>.  
  
## Example  
  
```  
// store_clipboard.cpp  
// compile with: /clr  
#using <System.dll>  
#using <System.Drawing.dll>  
#using <System.Windows.Forms.dll>  
  
using namespace System;  
using namespace System::Windows::Forms;  
  
[STAThread] int main()  
{  
   String^ str = "This text is copied into the Clipboard.";  
  
   // Use 'true' as the second argument if  
   // the data is to remain in the clipboard  
   // after the program terminates.  
   Clipboard::SetDataObject(str, true);  
  
   Console::WriteLine("Added text to the Clipboard.");  
  
   return 0;  
}  
```  
  
## See Also  
 [How to: Retrieve Text from the Clipboard (C++/CLI)](../vs140/How-to--Retrieve-Text-from-the-Clipboard--C---CLI-.md)   
 [Windows Operations in C++](../Topic/Windows%20Operations%20\(C++-CLI\).md)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)