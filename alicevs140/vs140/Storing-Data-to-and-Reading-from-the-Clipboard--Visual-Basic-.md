---
title: "Storing Data to and Reading from the Clipboard (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f690119a-4378-4f7d-b20e-d9377ef49496
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Storing Data to and Reading from the Clipboard (Visual Basic)
The Clipboard can be used to store data, such as text and images. Because the Clipboard is shared by all active processes, it can be used to transfer data between them. The `My.Computer.Clipboard` object allows you to easily access the Clipboard and to read from and write to it.  
  
## Reading from the Clipboard  
 Use the <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetText?qualifyHint=False> method to read the text in the Clipboard. The following code reads the text and displays it in a message box. There must be text stored on the Clipboard for the example to run correctly.  
  
 [!CODE [VbVbcnMyClipboard#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyClipboard#4)]  
  
 This code example is also available as an IntelliSense code snippet. In the code snippet picker, it is located in **Windows Forms Applications > Clipboard**. For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
 Use the <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetImage?qualifyHint=False> method to retrieve an image from the Clipboard. This example checks to see if there is an image on the Clipboard before retrieving it and assigning it to `PictureBox1`.  
  
 [!CODE [VbResourceTasks#16](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#16)]  
  
 This code example is also available as an IntelliSense code snippet. In the code snippet picker, it is located in **Windows Forms Applications > Clipboard**.For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
 Items placed on the Clipboard will persist even after the application is shut down.  
  
## Determining the type of file stored in the Clipboard  
 Data on the Clipboard may take a number of different forms, such as text, an audio file, or an image. In order to determine what sort of file is on the Clipboard, you can use methods such as <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsAudio?qualifyHint=False>, <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsFileDropList?qualifyHint=False>, <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsImage?qualifyHint=False>, and <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsText?qualifyHint=False>. The <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsData?qualifyHint=False> method can be used if you have a custom format that you want to check.  
  
 Use the `ContainsImage` function to determine whether the data contained on the Clipboard is an image. The following code checks to see whether the data is an image and reports accordingly.  
  
 [!CODE [VbResourceTasks#13](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#13)]  
  
## Clearing the Clipboard  
 The <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.Clear?qualifyHint=False> method clears the Clipboard. Because the Clipboard is shared by other processes, clearing it may have an impact on those processes.  
  
 The following code shows how to use the `Clear` method.  
  
 [!CODE [VbVbcnMyClipboard#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyClipboard#3)]  
  
## Writing to the Clipboard  
 Use the <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetText?qualifyHint=False> method to write text to the Clipboard. The following code writes the string "This is a test string" to the Clipboard.  
  
 [!CODE [VbVbcnMyClipboard#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyClipboard#1)]  
  
 The `SetText` method can accept a format parameter that contains a type of <xref:System.Windows.Forms.TextDataFormat?qualifyHint=False>. The following code writes the string "This is a test string" to the Clipboard as RTF text.  
  
 [!CODE [VbVbcnMyClipboard#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyClipboard#2)]  
  
 Use the <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetData?qualifyHint=False> method to write data to the Clipboard. This example writes the `DataObject``dataChunk` to the Clipboard in the custom format `specialFormat`.  
  
 [!CODE [VbVbcnMyClipboard#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyClipboard#7)]  
  
 Use the <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetAudio?qualifyHint=False> method to write audio data to the Clipboard. This example creates the byte array `musicReader`, reads the file `cool.wav` into it, and then writes it to the Clipboard.  
  
 [!CODE [VbResourceTasks#5](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#5)]  
  
> [!IMPORTANT]
>  Because the Clipboard can be accessed by other users, do not use it to store sensitive information, such as passwords or confidential data.  
  
## See Also  
 <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetAudioStream?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetDataObject?qualifyHint=False>   
 [How to: Read Object Data from an XML File in Visual Basic](../vs140/How-to--Read-Object-Data-from-an-XML-File--C#-and-Visual-Basic-.md)   
 [How to: Write Object Data to an XML File in Visual Basic](../vs140/How-to--Write-Object-Data-to-an-XML-File--C#-and-Visual-Basic-.md)