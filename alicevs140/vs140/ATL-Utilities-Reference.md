---
title: "ATL Utilities Reference"
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
ms.assetid: dd8a2888-34f4-461e-9bf4-834218f9b95b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Utilities Reference
ATL provides code for manipulating paths and URLs in the form of [CPathT](../vs140/CPathT-Class.md) and [CUrl](../vs140/CUrl-Class.md). A thread pool, [CThreadPool](../vs140/CThreadPool-Class.md), can be used in your applications. This code can be found in atlpath.h and atlutil.h.  
  
### Classes  
  
|||  
|-|-|  
|[CPathT Class](../vs140/CPathT-Class.md)|This class represents a path.|  
|[CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)|Use this class to send debug reports to a named pipe.|  
|[CNonStatelessWorker Class](../vs140/CNonStatelessWorker-Class.md)|Receives requests from a thread pool and passes them on to a worker object that is created and destroyed on each request.|  
|[CNoWorkerThread Class](../vs140/CNoWorkerThread-Class.md)|Use this class as the argument for the `MonitorClass` template parameter to cache classes if you want to disable dynamic cache maintenance.|  
|[CThreadPool Class](../vs140/CThreadPool-Class.md)|This class provides a pool of worker threads that process a queue of work items.|  
|[CUrl Class](../vs140/CUrl-Class.md)|This class represents a URL. It allows you to manipulate each element of the URL independently of the others whether parsing an existing URL string or building a string from scratch.|  
|[CWorkerThread Class](../vs140/CWorkerThread-Class.md)|This class creates a worker thread or uses an existing one, waits on one or more kernel object handles, and executes a specified client function when one of the handles is signaled.|  
  
### Typedefs  
  
|||  
|-|-|  
|[CPath](../vs140/CPath.md)|A specialization of [CPathT](../vs140/CPathT-Class.md) using `CString`.|  
|[CPathA](../vs140/CPathA.md)|A specialization of [CPathT](../vs140/CPathT-Class.md) using `CStringA`.|  
|[CPathW](../vs140/CPathW.md)|A specialization of [CPathT](../vs140/CPathT-Class.md) using `CStringW`.|  
|[ATL_URL_PORT](../vs140/ATL_URL_PORT.md)|The type used by [CUrl](../vs140/CUrl-Class.md) for specifying a port number.|  
  
### Enums  
  
|||  
|-|-|  
|[ATL_URL_SCHEME](../vs140/ATL_URL_SCHEME.md)|The members of this enumeration provide constants for the schemes understood by [CUrl](../vs140/CUrl-Class.md).|  
  
### Functions  
  
|||  
|-|-|  
|[AtlCanonicalizeUrl](../vs140/AtlCanonicalizeUrl.md)|Call this function to canonicalize a URL, which includes converting unsafe characters and spaces into escape sequences.|  
|[AtlCombineUrl](../vs140/AtlCombineUrl.md)|Call this function to combine a base URL and a relative URL into a single, canonical URL.|  
|[AtlEscapeUrl](../vs140/AtlEscapeUrl.md)|Call this function to convert all unsafe characters to escape sequences.|  
|[AtlGetDefaultUrlPort](../vs140/AtlGetDefaultUrlPort.md)|Call this function to get the default port number associated with a particular internet protocol or scheme.|  
|[AtlHexValue](../vs140/AtlHexValue.md)|Call this function to get the numeric value of a hexadecimal digit.|  
|[AtlIsUnsafeUrlChar](../vs140/AtlIsUnsafeUrlChar.md)|Call this function to find out whether a character is safe for use in a URL.|  
|[AtlUnescapeUrl](../vs140/AtlUnescapeUrl.md)|Call this function to convert escaped characters back to their original values.|  
|[SystemTimeToHttpDate](../vs140/SystemTimeToHttpDate.md)|Call this function to convert a system time to a string in a format suitable for using in HTTP headers.|  
|[ATLPath::AddBackslash](../vs140/ATLPath--AddBackslash.md)|This function is an overloaded wrapper for [PathAddBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773561).|  
|[ATLPath::AddExtension](../vs140/ATLPath--AddExtension.md)|This function is an overloaded wrapper for [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563).|  
|[ATLPath::Append](../vs140/ATLPath--Append.md)|This function is an overloaded wrapper for [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565).|  
|[ATLPath::BuildRoot](../vs140/ATLPath--BuildRoot.md)|This function is an overloaded wrapper for [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567).|  
|[ATLPath::Canonicalize](../vs140/ATLPath--Canonicalize.md)|This function is an overloaded wrapper for [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569).|  
|[ATLPath::Combine](../vs140/ATLPath--Combine.md)|This function is an overloaded wrapper for [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571).|  
|[ATLPath::CommonPrefix](../vs140/ATLPath--CommonPrefix.md)|This function is an overloaded wrapper for [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574).|  
|[ATLPath::CompactPath](../vs140/ATLPath--CompactPath.md)|This function is an overloaded wrapper for [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575).|  
|[ATLPath::CompactPathEx](../vs140/ATLPath--CompactPathEx.md)|This function is an overloaded wrapper for [PathCompactPathEx](http://msdn.microsoft.com/library/windows/desktop/bb773578).|  
|[ATLPath::FileExists](../vs140/ATLPath--FileExists.md)|This function is an overloaded wrapper for [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584).|  
|[ATLPath::FindExtension](../vs140/ATLPath--FindExtension.md)|This function is an overloaded wrapper for [PathFindExtension](http://msdn.microsoft.com/library/windows/desktop/bb773587).|  
|[ATLPath::FindFileName](../vs140/ATLPath--FindFileName.md)|This function is an overloaded wrapper for [PathFindFileName](http://msdn.microsoft.com/library/windows/desktop/bb773589).|  
|[ATLPath::GetDriveNumber](../vs140/ATLPath--GetDriveNumber.md)|This function is an overloaded wrapper for [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612).|  
|[ATLPath::IsDirectory](../vs140/ATLPath--IsDirectory.md)|This function is an overloaded wrapper for [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621).|  
|[ATLPath::IsFileSpec](../vs140/ATLPath--IsFileSpec.md)|This function is an overloaded wrapper for [PathIsFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773627).|  
|[ATLPath::IsPrefix](../vs140/ATLPath--IsPrefix.md)|This function is an overloaded wrapper for [PathIsPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773650).|  
|[ATLPath::IsRelative](../vs140/ATLPath--IsRelative.md)|This function is an overloaded wrapper for [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660).|  
|[ATLPath::IsRoot](../vs140/ATLPath--IsRoot.md)|This function is an overloaded wrapper for [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674).|  
|[ATLPath::IsSameRoot](../vs140/ATLPath--IsSameRoot.md)|This function is an overloaded wrapper for [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687).|  
|[ATLPath::IsUNC](../vs140/ATLPath--IsUNC.md)|This function is an overloaded wrapper for [PathIsUNC](http://msdn.microsoft.com/library/windows/desktop/bb773712).|  
|[ATLPath::IsUNCServer](../vs140/ATLPath--IsUNCServer.md)|This function is an overloaded wrapper for [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722).|  
|[ATLPath::IsUNCServerShare](../vs140/ATLPath--IsUNCServerShare.md)|This function is an overloaded wrapper for [PathIsUNCServerShare](http://msdn.microsoft.com/library/windows/desktop/bb773723).|  
|[ATLPath::MakePretty](../vs140/ATLPath--MakePretty.md)|This function is an overloaded wrapper for [PathMakePretty](http://msdn.microsoft.com/library/windows/desktop/bb773725).|  
|[ATLPath::MatchSpec](../vs140/ATLPath--MatchSpec.md)|This function is an overloaded wrapper for [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727).|  
|[ATLPath::QuoteSpaces](../vs140/ATLPath--QuoteSpaces.md)|This function is an overloaded wrapper for [PathQuoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773739).|  
|[ATLPath::RelativePathTo](../vs140/ATLPath--RelativePathTo.md)|This function is an overloaded wrapper for [PathRelativePathTo](http://msdn.microsoft.com/library/windows/desktop/bb773740).|  
|[ATLPath::RemoveArgs](../vs140/ATLPath--RemoveArgs.md)|This function is an overloaded wrapper for [PathRemoveArgs](http://msdn.microsoft.com/library/windows/desktop/bb773742).|  
|[ATLPath::RemoveBackslash](../vs140/ATLPath--RemoveBackslash.md)|This function is an overloaded wrapper for [PathRemoveBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773743).|  
|[ATLPath::RemoveBlanks](../vs140/ATLPath--RemoveBlanks.md)|This function is an overloaded wrapper for [PathRemoveBlanks](http://msdn.microsoft.com/library/windows/desktop/bb773745).|  
|[ATLPath::RemoveExtension](../vs140/ATLPath--RemoveExtension.md)|This function is an overloaded wrapper for [PathRemoveExtension](http://msdn.microsoft.com/library/windows/desktop/bb773746).|  
|[ATLPath::RemoveFileSpec](../vs140/ATLPath--RemoveFileSpec.md)|This function is an overloaded wrapper for [PathRemoveFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773748).|  
|[ATLPath::RenameExtension](../vs140/ATLPath--RenameExtension.md)|This function is an overloaded wrapper for [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749).|  
|[ATLPath::SkipRoot](../vs140/ATLPath--SkipRoot.md)|This function is an overloaded wrapper for [PathSkipRoot](http://msdn.microsoft.com/library/windows/desktop/bb773754).|  
|[ATLPath::StripPath](../vs140/ATLPath--StripPath.md)|This function is an overloaded wrapper for [PathStripPath](http://msdn.microsoft.com/library/windows/desktop/bb773756).|  
|[ATLPath::StripToRoot](../vs140/ATLPath--StripToRoot.md)|This function is an overloaded wrapper for [PathStripToRoot](http://msdn.microsoft.com/library/windows/desktop/bb773757).|  
|[ATLPath::UnquoteSpaces](../vs140/ATLPath--UnquoteSpaces.md)|This function is an overloaded wrapper for [PathUnquoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773763).|  
  
### Macros  
  
|||  
|-|-|  
|[ATL_URL Flags](../vs140/ATL_URL-Flags.md)|These flags modify the behavior of [AtlEscapeUrl](../vs140/AtlEscapeUrl.md) and [AtlCanonicalizeUrl](../vs140/AtlCanonicalizeUrl.md) .|  
|[ATL_WORKER_THREAD_WAIT](../vs140/ATL_WORKER_THREAD_WAIT.md)|This macro defines the default value in milliseconds that [CWorkerThread::Shutdown](../vs140/CWorkerThread--Shutdown.md) will wait for the worker thread to shut down.|  
|[ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT](../vs140/ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT.md)|This macro defines the default time in milliseconds that [CThreadPool](../vs140/CThreadPool-Class.md) will wait for a thread to shut down.|  
|[ATLS_DEFAULT_THREADSPERPROC](../vs140/ATLS_DEFAULT_THREADSPERPROC.md)|This macro defines the default number of threads per processor used by [CThreadPool](../vs140/CThreadPool-Class.md).|  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)