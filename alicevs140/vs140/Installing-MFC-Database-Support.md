---
title: "Installing MFC Database Support"
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
ms.assetid: a6c2fc84-9e0e-4f39-a464-0bcbc415b946
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Installing MFC Database Support
##  <a name="_core_odbc_drivers_installed"></a> ODBC Drivers Installed  
 Setup installs the following ODBC drivers:  
  
-   Microsoft Access driver  
  
-   Microsoft dBASE driver  
  
-   Microsoft Excel driver  
  
-   Microsoft FoxPro VFP driver  
  
-   Microsoft Visual FoxPro driver  
  
-   Microsoft ODBC for Oracle driver  
  
-   Microsoft Paradox driver  
  
-   Microsoft Text driver  
  
-   Microsoft SQL Server driver  
  
 For information about obtaining additional drivers and for a list of ODBC drivers included in this version of Visual C++, see [ODBC Driver List](../vs140/ODBC-Driver-List.md).  
  
##  <a name="_core_odbc_sdk_components_installed"></a> ODBC SDK Components Installed  
 Visual C++ includes many key ODBC components, including the required header files, libraries, DLLs, and tools. These include the ODBC Administrator Control Panel application, which you use to configure ODBC data sources, and the ODBC driver manager. Also included are ODBC drivers for many popular DBMSs, as listed in [ODBC Drivers Installed](#_core_odbc_drivers_installed).  
  
 The ODBC SDK gives you additional information and tools for writing and testing ODBC drivers. Note that as of Visual C++ .NET, the ODBC SDK is no longer included on the Visual C++ .NET installation media and is available as part of the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] installed with the Visual Studio .NET Prerequisites.  
  
##  <a name="_core_dao_sdk_components_installed"></a> DAO SDK Components Installed  
  
> [!NOTE]
>  Microsoft recommends using OLE DB or ODBC for new projects. DAO should only be used in maintaining existing applications.  
  
 The following components of the DAO SDK are installed by default:  
  
-   Microsoft Jet (4.0 SP3)  
  
-   Microsoft Jet (3.x MDB)  
  
-   Microsoft Jet (1.x, 2.x)  
  
-   All the database formats listed under [What Databases Can I Access with DAO and ODBC?](../vs140/What-Data-Sources-Can-I-Access-with-DAO-and-ODBC-.md)  
  
 In Visual C++ .NET, the DAO SDK is installed with the Visual Studio .NET Prerequisites. Run \Jet\Jetsetup.exe.  
  
> [!NOTE]
>  Microsoft recommends that you use Jet 4.0 Service Pack 3 (version 2927.04) or later. Jet 4.0 Service Pack 3 shipped with Windows 2000 and Windows ME. Using this version of Jet reduces the number of Jet versions that must be tested with your application. Windows XP might ship with another version of Jet. See "Note on Redistributing DAO Components" in [Redistributing Controls](../vs140/Redistributing-Controls.md).  
  
 If you want to install other DAO SDK components, such as the DAO SDK C++ classes, example files, or the Windows Help version of the DAO Help file, install the DAO SDK from the Visual C++ 6.0 CD-ROM.  
  
 For updates to and news about OLE DB, see the Universal Data Access Web site at [http://go.microsoft.com/fwlink/?LinkId=121548](http://go.microsoft.com/fwlink/?LinkId=121548).  
  
## See Also  
 [Data Access Programming (MFC/ATL)](../vs140/Data-Access-Programming--MFC-ATL-.md)