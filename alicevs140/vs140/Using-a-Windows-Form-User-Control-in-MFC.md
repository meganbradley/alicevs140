---
title: "Using a Windows Form User Control in MFC"
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
ms.assetid: 63fb099b-1dff-469c-9e34-dab52e122fcd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using a Windows Form User Control in MFC
Using the MFC Windows Forms support classes, you can host Windows Forms controls within your MFC applications as an ActiveX control within MFC dialog boxes or views. In addition, Windows Forms forms can be hosted as MFC dialog boxes.  
  
 The following sections describe how to:  
  
-   Host a Windows Forms control in an MFC dialog box.  
  
-   Host a Windows Forms user control as an MFC view.  
  
-   Host a Windows Forms form as an MFC dialog box.  
  
> [!NOTE]
>  MFC Windows Forms integration works only in projects that link dynamically with MFC (projects in which AFXDLL is defined).  
  
> [!NOTE]
>  When you build your application using a private (modified) copy of the MFC Windows Forms interfaces DLL (mfcmifc80.dll), it will fail to install in the GAC unless you replace the Microsoft key with your own vendor key. For more information on assembly signing, see [Programming with Assemblies](assetId:///25918b15-701d-42c7-95fc-c290d08648d6) and [Strong Name Assemblies (Assembly Signing)](../Topic/Strong%20Name%20Assemblies%20\(Assembly%20Signing\)%20\(C++-CLI\).md).  
  
 For sample applications using Windows Forms, see [BirthdayPicker Sample: Demonstrates .NET Framework Resources with Windows Forms](assetId:///ac932aed-5502-4667-be29-709bca435317), [Calculator Sample: Windows Forms Pocket Calculator](assetId:///2283b516-3b7e-45f2-80c4-fdcfb366ce25), and [Scribble Sample: MDI Drawing Application](assetId:///f025da3e-659b-4222-b991-554a1b8b2358).  
  
 For a sample application that shows Windows Forms used with MFC, see [MFC and Windows Forms Integration](http://www.microsoft.com/downloads/details.aspx?FamilyID=987021bc-e575-4fe3-baa9-15aa50b0f599&displaylang=en).  
  
 If your MFC application uses Windows Forms, you need to redistribute mfcmifc90.dll with your application. For more information, see [Redistributing the MFC Library](../vs140/Redistributing-the-MFC-Library.md).  
  
## In This Section  
 [Hosting a Windows Forms Control in an MFC Dialog Box](../Topic/Hosting%20a%20Windows%20Form%20User%20Control%20in%20an%20MFC%20Dialog%20Box.md)  
  
 [Hosting a Windows Forms User Control as an MFC View](../vs140/Hosting-a-Windows-Forms-User-Control-as-an-MFC-View.md)  
  
 [Hosting a Windows Forms Form as an MFC Dialog Box](../Topic/Hosting%20a%20Windows%20Form%20User%20Control%20as%20an%20MFC%20Dialog%20Box.md)  
  
## Reference  
 [CWinFormsControl Class](../vs140/CWinFormsControl-Class.md)  
  
 [CWinFormsDialog Class](../Topic/CWinFormsDialog%20Class.md)  
  
 [CWinFormsView Class](../Topic/CWinFormsView%20Class.md)  
  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)  
  
 [ICommandTarget Interface](../vs140/ICommandTarget-Interface.md)  
  
 [ICommandUI Interface](../vs140/ICommandUI-Interface.md)  
  
 [IView Interface](../vs140/IView-Interface.md)  
  
 [CommandHandler Delegate](../vs140/CommandHandler-Delegate.md)  
  
 [CommandUIHandler Delegate](../vs140/CommandUIHandler-Delegate.md)  
  
 [DDX_ManagedControl](../vs140/DDX_ManagedControl.md)  
  
 [UICheckState Enumeration](../vs140/UICheckState-Enumeration.md)  
  
## Related Sections  
 [Windows Forms](assetId:///627df1e9-b254-41af-bbac-9a4f02810c54)  
  
 [Windows Forms Controls](assetId:///f050de8f-4ebd-4042-94b8-edf9a1dbd52a)  
  
 [Web Forms User Controls](assetId:///5e601b3d-bb16-4dbe-9e35-7e92a34565ca)  
  
## See Also  
 [User Interface](../vs140/User-Interface-Elements--MFC-.md)   
 [Form Topics](../vs140/Form-Views--MFC-.md)