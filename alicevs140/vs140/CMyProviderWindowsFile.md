---
title: "CMyProviderWindowsFile"
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
ms.assetid: 0e9e72ac-1e1e-445f-a7ac-690c20031f9d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMyProviderWindowsFile
The wizard creates a class to contain one row of data; in this case, it is called `CMyProviderWindowsFile`. The following code for `CMyProviderWindowsFile` is wizard generated and lists all the files in a directory by using the **WIN32_FIND_DATA** structure. `CMyProviderWindowsFile` inherits from the **WIN32_FIND_DATA** structure:  
  
```  
/////////////////////////////////////////////////////////////////////  
// MyProviderRS.H  
  
class CMyProviderWindowsFile:   
   public WIN32_FIND_DATA  
{  
public:  
BEGIN_PROVIDER_COLUMN_MAP(CMyProviderWindowsFile)  
   PROVIDER_COLUMN_ENTRY("FileAttributes", 1, dwFileAttributes)  
   PROVIDER_COLUMN_ENTRY("FileSizeHigh", 2, nFileSizeHigh)  
   PROVIDER_COLUMN_ENTRY("FileSizeLow", 3, nFileSizeLow)  
   PROVIDER_COLUMN_ENTRY_STR("FileName", 4, cFileName)  
   PROVIDER_COLUMN_ENTRY_STR("AltFileName", 5, cAlternateFileName)  
END_PROVIDER_COLUMN_MAP()  
};  
```  
  
 `CMyProviderWindowsFile` is called the [user record class](../vs140/User-Record.md) because it also contains a map describing the columns in the provider's rowset. The provider column map contains one entry for each field in the rowset using the PROVIDER_COLUMN_ENTRY macros. The macros specify column name, ordinal, and offset to a structure entry. The provider column entries in the above code contain offsets into the **WIN32_FIND_DATA** structure. When the consumer calls **IRowset::GetData**, data is transferred in one contiguous buffer. Rather than making you do pointer arithmetic, the map allows you to specify a data member.  
  
 The `CMyProviderRowset` class also contains the `Execute` method. `Execute` is what actually reads the data in from the native source. The following code shows the wizard-generated `Execute` method. The function uses the Win32 **FindFirstFile** and `FindNextFile` APIs to retrieve information about the files in the directory and place them in instances of the `CMyProviderWindowsFile` class.  
  
```  
/////////////////////////////////////////////////////////////////////  
// MyProviderRS.H  
  
HRESULT Execute(DBPARAMS * pParams, LONG* pcRowsAffected)  
{  
   USES_CONVERSION;  
   BOOL bFound = FALSE;  
   HANDLE hFile;  
   LPTSTR  szDir = (m_strCommandText == _T("")) ? _T("*.*") :  
       OLE2T(m_strCommandText);  
   CMyProviderWindowsFile wf;  
   hFile = FindFirstFile(szDir, &wf);  
   if (hFile == INVALID_HANDLE_VALUE)  
      return DB_E_ERRORSINCOMMAND;  
   LONG cFiles = 1;  
   BOOL bMoreFiles = TRUE;  
   while (bMoreFiles)  
   {  
      if (!m_rgRowData.Add(wf))  
         return E_OUTOFMEMORY;  
      bMoreFiles = FindNextFile(hFile, &wf);  
      cFiles++;  
   }  
   FindClose(hFile);  
   if (pcRowsAffected != NULL)  
      *pcRowsAffected = cFiles;  
   return S_OK;  
}  
```  
  
 The directory to search is represented by `m_strCommandText`; this contains the text represented by the `ICommandText` interface in the command object. If no directory is specified, it uses the current directory.  
  
 The method creates one entry for each file (corresponding to a row) and places it in the **m_rgRowData** data member. The `CRowsetImpl` class defines the **m_rgRowData** data member. The data in this array represents the entire table and is used throughout the templates.  
  
## See Also  
 [Provider Wizard-Generated Files](../vs140/Provider-Wizard-Generated-Files.md)