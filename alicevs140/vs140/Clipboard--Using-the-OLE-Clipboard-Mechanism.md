---
title: "Clipboard: Using the OLE Clipboard Mechanism"
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
ms.assetid: 229cc610-5bb1-435e-bd20-2c8b9964d1af
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Clipboard: Using the OLE Clipboard Mechanism
OLE uses standard formats and some OLE-specific formats for transferring data through the Clipboard.  
  
 When you cut or copy data from an application, the data is stored on the Clipboard to be used later in paste operations. This data is in a variety of formats. When a user chooses to paste data from the Clipboard, the application can choose which of these formats to use. The application should be written to choose the format that provides the most information, unless the user specifically asks for a certain format, using Paste Special. Before continuing, you may want to read the [Data Objects and Data Sources (OLE)](../vs140/Data-Objects-and-Data-Sources--OLE-.md) topics. They describe the fundamentals of how data transfers work, and how to implement them in your applications.  
  
 Windows defines a number of standard formats that can be used for transferring data through the Clipboard. These include metafiles, text, bitmaps, and others. OLE defines a number of OLE-specific formats, as well. For applications that need more detail than given by these standard formats, it is a good idea to register their own custom Clipboard formats. Use the Win32 API function [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) to do this.  
  
 For example, Microsoft Excel registers a custom format for spreadsheets. This format carries much more information than, for example, a bitmap does. When this data is pasted into an application that supports the spreadsheet format, all the formulas and values from the spreadsheet are retained and can be updated if necessary. Microsoft Excel also puts data on the Clipboard in formats so that it can be pasted as an OLE item. Any OLE document container can paste this information as an embedded item. This embedded item can be changed using Microsoft Excel. The Clipboard also contains a simple bitmap of the image of the selected range on the spreadsheet. This can also be pasted into OLE document containers or into bitmap editors, like Paint. In the case of a bitmap, however, there is no way to manipulate the data as a spreadsheet.  
  
 To retrieve the maximum amount of information from the Clipboard, applications should check for these custom formats before pasting data from the Clipboard.  
  
 For example, to enable the Cut command, you might write a handler something like the following:  
  
 [!CODE [NVC_MFCListView#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#3)]  
  
## What do you want to know more about?  
  
-   [Copying and pasting data](../vs140/Clipboard--Copying-and-Pasting-Data.md)  
  
-   [Adding other formats](../vs140/Clipboard--Adding-Other-Formats.md)  
  
-   [Using the Windows Clipboard](../vs140/Clipboard--Using-the-Windows-Clipboard.md)  
  
-   [OLE](../vs140/OLE-Background.md)  
  
-   [OLE data objects and data sources and uniform data transfer](../vs140/Data-Objects-and-Data-Sources--OLE-.md)  
  
## See Also  
 [Clipboard](../vs140/Clipboard.md)