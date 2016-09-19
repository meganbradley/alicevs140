---
title: "ATL Functions Alphabetical Reference"
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
ms.topic: reference
ms.assetid: 8968fe02-2a8a-4b72-9c58-c6c19e9f703c
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Functions Alphabetical Reference
In this section, reference topics for the ATL global functions are organized alphabetically. To find a particular function by category, see [ATL Functions](../vs140/ATL-Functions.md).  
  
|Function|Description|  
|--------------|-----------------|  
|[AtlAdvise](../vs140/AtlAdvise.md)|Creates a connection between an object's connection point and a client's sink.|  
|[AtlAdviseSinkMap](../vs140/AtlAdviseSinkMap.md)|Call this function to advise or unadvise all entries in the object's sink event map.|  
|[AtlAxAttachControl](../vs140/AtlAxAttachControl.md)|Attaches a previously created control to the specified window.|  
|[AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md)|Creates an ActiveX control, initializes it, and hosts it in the specified window. An interface pointer and event sink for the new control can also be created.|  
|[AtlAxCreateControlLicEx](../vs140/AtlAxCreateControlLicEx.md)|Creates a licensed ActiveX control, initializes it, and hosts it in the specified window. An interface pointer and event sink for the new control can also be created.|  
|[AtlAxCreateControlLic](../vs140/AtlAxCreateControlLic.md)|Creates a licensed ActiveX control, initializes it, and hosts it in the specified window.|  
|[AtlAxCreateControl](../vs140/AtlAxCreateControl.md)|Creates an ActiveX control, initializes it, and hosts it in the specified window.|  
|[AtlAxCreateDialog](../vs140/AtlAxCreateDialog.md)|Creates a modeless dialog box from a dialog template provided by the user.|  
|[AtlAxDialogBox](../vs140/AtlAxDialogBox.md)|Creates a modal dialog box from a dialog template provided by the user.|  
|[AtlAxGetControl](../vs140/AtlAxGetControl.md)|Obtains a direct interface pointer to the control contained inside a specified window given its handle.|  
|[AtlAxGetHost](../vs140/AtlAxGetHost.md)|Obtains a direct interface pointer to the container for a specified window (if any), given its handle.|  
|[AtlAxWinInit](../vs140/AtlAxWinInit.md)|This function initializes ATL's control hosting code by registering the **"AtlAxWin80"** and **"AtlAxWinLic80"** window classes plus a couple of custom window messages.|  
|[AtlAxWinTerm](../vs140/AtlAxWinTerm.md)|This function uninitializes ATL's control hosting code by unregistering the **"AtlAxWin80"** and **"AtlAxWinLic80"** window classes.|  
|[AtlCanonicalizeUrl](../vs140/AtlCanonicalizeUrl.md)|Call this function to canonicalize a URL, which includes converting unsafe characters and spaces into escape sequences.|  
|[AtlCombineUrl](../vs140/AtlCombineUrl.md)|Call this function to combine a base URL and a relative URL into a single, canonical URL.|  
|[AtlComModuleGetClassObject](../vs140/AtlComModuleGetClassObject.md)|This function is called to return the class factory.|  
|[AtlComModuleRegisterClassObjects](../vs140/AtlComModuleRegisterClassObjects.md)|This function is called to register class objects.|  
|[AtlComModuleRegisterServer](../vs140/AtlComModuleRegisterServer.md)|This function is called to register every object in the object map.|  
|[AtlComModuleRevokeClassObjects](../vs140/AtlComModuleRevokeClassObjects.md)|This function is called to remove the class factory/factories from the Running Object Table.|  
|[AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md)|This function is called to unregister every object in the object map.|  
|[AtlComPtrAssign](../vs140/AtlComPtrAssign.md)|Assigns an interface pointer to another interface pointer of the same type.|  
|[AtlComQIPtrAssign](../vs140/AtlComQIPtrAssign.md)|Assigns an interface pointer to another interface pointer of a different type.|  
|[AtlCreateTargetDC](../vs140/AtlCreateTargetDC.md)|Creates a device context for the device specified in the [DVTARGETDEVICE](http://msdn.microsoft.com/library/windows/desktop/ms686613) structure.|  
|[AtlEscapeUrl](../vs140/AtlEscapeUrl.md)|Call this function to convert all unsafe characters to escape sequences.|  
|[AtlFreeMarshalStream](../vs140/AtlFreeMarshalStream.md)|Releases the marshal data in the stream, then releases the stream pointer.|  
|[AtlGetDacl](../vs140/AtlGetDacl.md)|Call this function to retrieve the discretionary access-control list (DACL) information of a specified object.|  
|[AtlGetDefaultUrlPort](../vs140/AtlGetDefaultUrlPort.md)|Call this function to get the default port number associated with a particular Internet protocol or scheme.|  
|[AtlGetGroupSid](../vs140/AtlGetGroupSid.md)|Call this function to retrieve the group security identifier (SID) of an object.|  
|[AtlGetHexValue](../vs140/AtlGetHexValue.md)|Call this function to get the numeric value of a hexadecimal digit.|  
|[AtlGetObjectSourceInterface](../vs140/AtlGetObjectSourceInterface.md)|Call this function to retrieve information about the default source interface of an object.|  
|[AtlGetOwnerSid](../vs140/AtlGetOwnerSid.md)|Call this function to retrieve the owner security identifier (SID) of an object.|  
|[AtlGetPerUserRegistration](../vs140/AtlGetPerUserRegistration.md)|Use this function to determine whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
|[AtlGetSacl](../vs140/AtlGetSacl.md)|Call this function to retrieve the system access-control list (SACL) information of a specified object.|  
|[AtlGetSecurityDescriptor](../vs140/AtlGetSecurityDescriptor.md)|Call this function to retrieve the security descriptor of a given object.|  
|[AtlHexDecode](../vs140/AtlHexDecode.md)|Decodes a string of data that has been encoded as hexadecimal text such as by a previous call to [AtlHexEncode](../vs140/AtlHexEncode.md).|  
|[AtlHexDecodeGetRequiredLength](../vs140/AtlHexDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from a hex-encoded string of the specified length.|  
|[AtlHexEncode](../vs140/AtlHexEncode.md)|Call this function to encode some data as a string of hexadecimal text.|  
|[AtlHexEncodeGetRequiredLength](../vs140/AtlHexEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[AtlHexValue](../vs140/AtlHexValue.md)|Call this function to get the numeric value of a hexadecimal digit.|  
|[AtlHiMetricToPixel](../vs140/AtlHiMetricToPixel.md)|Converts an object's size in HIMETRIC units (each unit is 0.01 millimeter) to a size in pixels on the screen device.|  
|[AtlHresultFromLastError](../vs140/AtlHresultFromLastError.md)|Returns the calling thread's last-error code value in the form of an HRESULT.|  
|[AtlHresultFromWin32](../vs140/AtlHresultFromWin32.md)|Converts a Win32 error code into an HRESULT.|  
|[AtlInternalQueryInterface](../vs140/AtlInternalQueryInterface.md)|Retrieves a pointer to the requested interface.|  
|[AtlIsUnsafeUrlChar](../vs140/AtlIsUnsafeUrlChar.md)|Call this function to find out whether a character is safe for use in a URL.|  
|[AtlLoadTypeLib](../vs140/AtlLoadTypeLib.md)|This function is called to load a type library.|  
|[AtlMarshalPtrInProc](../vs140/AtlMarshalPtrInProc.md)|Creates a new stream object, writes the CLSID of the proxy to the stream, and marshals the specified interface pointer by writing the data needed to initialize the proxy into the stream.|  
|[AtlModuleRegisterServer](../vs140/AtlModuleRegisterServer.md)|Registers every object in the object map.|  
|[AtlModuleRegisterTypeLib](../vs140/AtlModuleRegisterTypeLib.md)|Registers a type library.|  
|[AtlModuleUnregisterServerEx](../vs140/AtlModuleUnregisterServerEx.md)|Unregisters every object in the object map.|  
|[AtlModuleUnregisterServer](../vs140/AtlModuleUnregisterServer.md)|Unregisters every object in the object map. It is similar to `AtlModuleUnregisterServerEx` except that it cannot unregister the type library.|  
|[AtlModuleUnregisterTypeLib](../vs140/AtlModuleUnregisterTypeLib.md)|Unregisters a type library.|  
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
|[AtlPixelToHiMetric](../vs140/AtlPixelToHiMetric.md)|Converts an object's size in pixels on the screen device to a size in HIMETRIC units (each unit is 0.01 millimeter).|  
|[AtlRegisterTypeLib](../vs140/AtlRegisterTypeLib.md)|This function is called to register a type library.|  
|[AtlReportError](../vs140/AtlReportError.md)|Sets up the [IErrorInfo](assetId:///4dda6909-2d9a-4727-ae0c-b5f90dcfa447) interface to provide error information to clients of the object.|  
|[AtlSetChildSite](../vs140/AtlSetChildSite.md)|Call this function to set the site of the child object to the **IUnknown** of the parent object.|  
|[AtlSetDacl](../vs140/AtlSetDacl.md)|Call this function to set the discretionary access-control list (DACL) information of a specified object.|  
|[AtlSetGroupSid](../vs140/AtlSetGroupSid.md)|Call this function to set the group security identifier (SID) of an object.|  
|[AtlSetOwnerSid](../vs140/AtlSetOwnerSid.md)|Call this function to set the owner security identifier (SID) of an object.|  
|[AtlSetPerUserRegistration](../vs140/AtlSetPerUserRegistration.md)|Sets whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
|[AtlSetSacl](../vs140/AtlSetSacl.md)|Call this function to set the system access-control list (SACL) information of a specified object.|  
|[AtlThrowLastWin32](../vs140/AtlThrowLastWin32.md)|Call this function to signal an error based on the result of the Windows function `GetLastError`.|  
|[AtlThrow](../vs140/AtlThrow.md)|Call this function to signal an error based on a `HRESULT` status code.|  
|[AtlUnadvise](../vs140/AtlUnadvise.md)|Terminates the connection established through [AtlAdvise](../vs140/AtlAdvise.md).|  
|[AtlUnescapeUrl](../vs140/AtlUnescapeUrl.md)|Call this function to convert escaped characters back to their original values.|  
|[AtlUnicodeToUTF8](../vs140/AtlUnicodeToUTF8.md)|Call this function to convert a Unicode string to UTF-8.|  
|[AtlUnmarshalPtr](../vs140/AtlUnmarshalPtr.md)|Converts the stream's marshaling data into an interface pointer that can be used by the client.|  
|[AtlUnRegisterTypeLib](../vs140/AtlUnRegisterTypeLib.md)|This function is called to unregister a type library.|  
|[AtlUpdateRegistryFromResourceD](../vs140/AtlUpdateRegistryFromResourceD.md) **<Removed\>**|This function was deprecated in earlier releases and is removed in Visual Studio 2015.|  
|[AtlWaitWithMessageLoop](../vs140/AtlWaitWithMessageLoop.md)|Waits for the object to be signaled, meanwhile dispatching window messages as needed.|  
|[AtlWinModuleAddCreateWndData](../vs140/AtlWinModuleAddCreateWndData.md)|This function is used to initialize and add an `_AtlCreateWndData` structure.|  
|[AtlWinModuleExtractCreateWndData](../vs140/AtlWinModuleExtractCreateWndData.md)|Call this function to extract an existing `_AtlCreateWndData` structure.|  
|[BEncode](../vs140/BEncode.md)|Call this function to convert some data using the "B" encoding.|  
|[BEncodeGetRequiredLength](../vs140/BEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[EscapeXML](../vs140/EscapeXML.md)|Call this function to convert characters that are unsafe for use in XML to their safe equivalents.|  
|[GetExtendedChars](../vs140/GetExtendedChars.md)|Call this function to get the number of extended characters in a string.|  
|[InlineIsEqualIUnknown](../vs140/InlineIsEqualIUnknown.md)|Call this function, for the special case of testing for **IUnknown**.|  
|[IsExtendedChar](../vs140/IsExtendedChar.md)|Call this function to find out if a given character is an extended character (less than 32, greater than 126, and not a tab, linefeed or carriage return)|  
|[QEncode](../vs140/QEncode.md)|Call this function to convert some data using the "Q" encoding.|  
|[QEncodeGetRequiredLength](../vs140/QEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[QPDecode](../vs140/QPDecode.md)|Decodes a string of data that has been encoded in quoted-printable format such as by a previous call to [QPEncode](../vs140/QPEncode.md).|  
|[QPDecodeGetRequiredLength](../vs140/QPDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from quoted-printable-encoded string of the specified length.|  
|[QPEncode](../vs140/QPEncode.md)|Call this function to encode some data in quoted-printable format.|  
|[QPEncodeGetRequiredLength](../vs140/QPEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[RegistryDataExchange](../vs140/RegistryDataExchange.md)|This function is called to read from, or write to, the system registry.|  
|[RGBToHtml](../vs140/RGBToHtml.md)|Converts a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value to the HTML text corresponding to that color value.|  
|[Sids::AccountOps](../vs140/Sids--AccountOps.md)|Returns the DOMAIN_ALIAS_RID_ACCOUNT_OPS SID.|  
|[Sids::Admins](../vs140/Sids--Admins.md)|Returns the DOMAIN_ALIAS_RID_ADMINS SID.|  
|[Sids::AnonymousLogon](../vs140/Sids--AnonymousLogon.md)|Returns the SECURITY_ANONYMOUS_LOGON_RID SID.|  
|[Sids::AuthenticatedUser](../vs140/Sids--AuthenticatedUser.md)|Returns the SECURITY_AUTHENTICATED_USER_RID SID.|  
|[Sids::BackupOps](../vs140/Sids--BackupOps.md)|Returns the DOMAIN_ALIAS_RID_BACKUP_OPS SID.|  
|[Sids::Batch](../vs140/Sids--Batch.md)|Returns the SECURITY_BATCH_RID SID.|  
|[Sids::CreatorGroupServer](../vs140/Sids--CreatorGroupServer.md)|Returns the SECURITY_CREATOR_GROUP_SERVER_RID SID.|  
|[Sids::CreatorGroup](../vs140/Sids--CreatorGroup.md)|Returns the SECURITY_CREATOR_GROUP_RID SID.|  
|[Sids::CreatorOwnerServer](../vs140/Sids--CreatorOwnerServer.md)|Returns the SECURITY_CREATOR_OWNER_SERVER_RID SID.|  
|[Sids::CreatorOwner](../vs140/Sids--CreatorOwner.md)|Returns the SECURITY_CREATOR_OWNER_RID SID.|  
|[Sids::Dialup](../vs140/Sids--Dialup.md)|Returns the SECURITY_DIALUP_RID SID.|  
|[Sids::Guests](../vs140/Sids--Guests.md)|Returns the DOMAIN_ALIAS_RID_GUESTS SID.|  
|[Sids::Interactive](../vs140/Sids--Interactive.md)|Returns the SECURITY_INTERACTIVE_RID SID.|  
|[Sids::Local](../vs140/Sids--Local.md)|Returns the SECURITY_LOCAL_RID SID.|  
|[Sids::Network](../vs140/Sids--Network.md)|Returns the SECURITY_NETWORK_RID SID.|  
|[Sids::NetworkService](../vs140/Sids--NetworkService.md)|Returns the SECURITY_NETWORK_SERVICE_RID SID.|  
|[Sids::Null](../vs140/Sids--Null.md)|Returns the SECURITY_NULL_RID SID.|  
|[Sids::PowerUsers](../vs140/Sids--PowerUsers.md)|Returns the DOMAIN_ALIAS_RID_POWER_USERS SID.|  
|[Sids::PreW2KAccess](../vs140/Sids--PreW2KAccess.md)|Returns the DOMAIN_ALIAS_RID_PREW2KCOMPACCESS SID.|  
|[Sids::PrintOps](../vs140/Sids--PrintOps.md)|Returns the DOMAIN_ALIAS_RID_PRINT_OPS SID.|  
|[Sids::Proxy](../vs140/Sids--Proxy.md)|Returns the SECURITY_PROXY_RID SID.|  
|[Sids::RasServers](../vs140/Sids--RasServers.md)|Returns the DOMAIN_ALIAS_RID_RAS_SERVERS SID.|  
|[Sids::Replicator](../vs140/Sids--Replicator.md)|Returns the DOMAIN_ALIAS_RID_REPLICATOR SID.|  
|[Sids::RestrictedCode](../vs140/Sids--RestrictedCode.md)|Returns the SECURITY_RESTRICTED_CODE_RID SID.|  
|[Sids::Self](../vs140/Sids--Self.md)|Returns the SECURITY_PRINCIPAL_SELF_RID SID.|  
|[Sids::ServerLogon](../vs140/Sids--ServerLogon.md)|Returns the SECURITY_SERVER_LOGON_RID SID.|  
|[Sids::Service](../vs140/Sids--Service.md)|Returns the SECURITY_SERVICE_RID SID.|  
|[Sids::SystemOps](../vs140/Sids--SystemOps.md)|Returns the DOMAIN_ALIAS_RID_SYSTEM_OPS SID.|  
|[Sids::System](../vs140/Sids--System.md)|Returns the SECURITY_LOCAL_SYSTEM_RID SID.|  
|[Sids::TerminalServer](../vs140/Sids--TerminalServer.md)|Returns the SECURITY_TERMINAL_SERVER_RID SID.|  
|[Sids::Users](../vs140/Sids--Users.md)|Returns the DOMAIN_ALIAS_RID_USERS SID.|  
|[Sids::World](../vs140/Sids--World.md)|Returns the SECURITY_WORLD_RID SID.|  
|[SystemTimeToHttpDate](../vs140/SystemTimeToHttpDate.md)|Call this function to convert a system time to a string in a format suitable for using in HTTP headers.|  
|[UUDecode](../vs140/UUDecode.md)|Decodes a string of data that has been uuencoded such as by a previous call to [UUEncode](../vs140/UUEncode.md).|  
|[UUDecodeGetRequiredLength](../vs140/UUDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from a uuencoded string of the specified length.|  
|[UUEncode](../vs140/UUEncode.md)|Call this function to uuencode some data.|  
|[UUEncodeGetRequiredLength](../vs140/UUEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|