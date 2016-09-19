---
title: "CTokenGroups Class"
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
ms.assetid: 2ab08076-4b08-4487-bc70-ec6dee304190
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenGroups Class
This class is a wrapper for the **TOKEN_GROUPS** structure.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CTokenGroups  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CTokenGroups::CTokenGroups](../vs140/CTokenGroups--CTokenGroups.md)|The constructor.|  
|[CTokenGroups::~CTokenGroups](../vs140/CTokenGroups--~CTokenGroups.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CTokenGroups::Add](../vs140/CTokenGroups--Add.md)|Adds a `CSid` or existing **TOKEN_GROUPS** structure to the `CTokenGroups` object.|  
|[CTokenGroups::Delete](../vs140/CTokenGroups--Delete.md)|Deletes a `CSid` and its associated attributes from the `CTokenGroups` object.|  
|[CTokenGroups::DeleteAll](../vs140/CTokenGroups--DeleteAll.md)|Deletes all `CSid` objects and their associated attributes from the `CTokenGroups` object.|  
|[CTokenGroups::GetCount](../vs140/CTokenGroups--GetCount.md)|Returns the number of `CSid` objects and associated attributes contained in the **CTokenGroups** object.|  
|[CTokenGroups::GetLength](../vs140/CTokenGroups--GetLength.md)|Returns the size of the `CTokenGroups` object.|  
|[CTokenGroups::GetPTOKEN_GROUPS](../vs140/CTokenGroups--GetPTOKEN_GROUPS.md)|Retrieves a pointer to the **TOKEN_GROUPS** structure.|  
|[CTokenGroups::GetSidsAndAttributes](../vs140/CTokenGroups--GetSidsAndAttributes.md)|Retrieves the `CSid` objects and attributes belonging to the `CTokenGroups` object.|  
|[CTokenGroups::LookupSid](../vs140/CTokenGroups--LookupSid.md)|Retrieves the attributes associated with a `CSid` object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CTokenGroups::operator const TOKEN_GROUPS*](../vs140/CTokenGroups--operator-const-TOKEN_GROUPS--.md)|Casts the `CTokenGroups` object to a pointer to the **TOKEN_GROUPS** structure.|  
|[CTokenGroups::operator=](../vs140/CTokenGroups--operator-=.md)|Assignment operator.|  
  
## Remarks  
 An [access token](http://msdn.microsoft.com/library/windows/desktop/aa374909) is an object that describes the security context of a process or thread and is allocated to each user logged onto a Windows NT or Windows 2000 system.  
  
 The **CTokenGroups** class is a wrapper for the [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure, containing information about the group security identifiers (SIDs) in an access token.  
  
 For an introduction to the access control model in Windows, see [Access Control](http://msdn.microsoft.com/library/windows/desktop/aa374860) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlsecurity.h  
  
##  <a name="ctokengroups__add"></a>  CTokenGroups::Add  
 Adds a `CSid` or existing **TOKEN_GROUPS** structure to the `CTokenGroups` object.  
  
```  
  
void Add(  
      const CSid &  rSid,  
      DWORD  dwAttributes  
   ) throw(...);  
   void Add(  
      const TOKEN_GROUPS &  rTokenGroups  
   ) throw(...);  
  
```  
  
### Parameters  
 `rSid`  
 A [CSid](../vs140/CSid-Class.md) object.  
  
 `dwAttributes`  
 The attributes to associate with the `CSid` object.  
  
 *rTokenGroups*  
 A [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure.  
  
### Remarks  
 These methods add one or more `CSid` objects and their associated attributes to the `CTokenGroups` object.  
  
##  <a name="ctokengroups__ctokengroups"></a>  CTokenGroups::CTokenGroups  
 The constructor.  
  
```  
  
CTokenGroups( ) throw( );   
   CTokenGroups(  
      const CTokenGroups &  rhs  
   ) throw(...);  
   CTokenGroups(  
      const TOKEN_GROUPS &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The `CTokenGroups` object or [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure with which to construct the `CTokenGroups` object.  
  
### Remarks  
 The `CTokenGroups` object can optionally be created using a **TOKEN_GROUPS** structure or a previously defined `CTokenGroups` object.  
  
##  <a name="ctokengroups___dtorctokengroups"></a>  CTokenGroups::~CTokenGroups  
 The destructor.  
  
```  
  
virtual ~CTokenGroups( ) throw( );  
  
```  
  
### Remarks  
 The destructor frees all allocated resources.  
  
##  <a name="ctokengroups__delete"></a>  CTokenGroups::Delete  
 Deletes a `CSid` and its associated attributes from the `CTokenGroups` object.  
  
```  
  
bool Delete(  
      const CSid &  rSid  
   ) throw( );  
  
```  
  
### Parameters  
 `rSid`  
 The [CSid](../vs140/CSid-Class.md) object for which the security identifier (SID) and attributes should be removed.  
  
### Return Value  
 Returns true if the `CSid` is removed, false otherwise.  
  
##  <a name="ctokengroups__deleteall"></a>  CTokenGroups::DeleteAll  
 Deletes all `CSid` objects and their associated attributes from the `CTokenGroups` object.  
  
```  
  
void DeleteAll( ) throw( );  
  
```  
  
##  <a name="ctokengroups__getcount"></a>  CTokenGroups::GetCount  
 Returns the number of `CSid` objects contained in `CTokenGroups`.  
  
```  
  
UINT GetCount( ) const throw( );  
  
```  
  
### Return Value  
 Returns the number of [CSid](../vs140/CSid-Class.md) objects and their associated attributes contained in the `CTokenGroups` object.  
  
##  <a name="ctokengroups__getlength"></a>  CTokenGroups::GetLength  
 Returns the size of the **CTokenGroup** object.  
  
```  
  
UINT GetLength( ) const throw( );  
  
```  
  
### Remarks  
 Returns the total size of the **CTokenGroup** object, in bytes.  
  
##  <a name="ctokengroups__getptoken_groups"></a>  CTokenGroups::GetPTOKEN_GROUPS  
 Retrieves a pointer to the **TOKEN_GROUPS** structure.  
  
```  
  
const TOKEN_GROUPS * GetPTOKEN_GROUPS( ) const throw(...);  
  
```  
  
### Return Value  
 Retrieves a pointer to the [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure belonging to the `CTokenGroups` access token object.  
  
##  <a name="ctokengroups__getsidsandattributes"></a>  CTokenGroups::GetSidsAndAttributes  
 Retrieves the `CSid` objects and (optionally) the attributes belonging to the `CTokenGroups` object.  
  
```  
  
void GetSidsAndAttributes(  
      CSid::CSidArray *  pSids,  
      CAtlArray< DWORD > *  pAttributes  
    = NULL  
   ) const throw(...);  
  
```  
  
### Parameters  
 `pSids`  
 Pointer to an array of [CSid](../vs140/CSid-Class.md) objects.  
  
 `pAttributes`  
 Pointer to an array of DWORDs. If this parameter is omitted or NULL, the attributes are not retrieved.  
  
### Remarks  
 This method will enumerate all of the `CSid` objects contained in the `CTokenGroups` object and place them and (optionally) the attribute flags into array objects.  
  
##  <a name="ctokengroups__lookupsid"></a>  CTokenGroups::LookupSid  
 Retrieves the attributes associated with a `CSid` object.  
  
```  
  
bool LookupSid(  
      const CSid &  rSid,  
      DWORD *  pdwAttributes  
    = NULL  
   ) const throw( );  
  
```  
  
### Parameters  
 `rSid`  
 The [CSid](../vs140/CSid-Class.md) object.  
  
 `pdwAttributes`  
 Pointer to a DWORD which will accept the `CSid` object's attribute. If omitted or NULL, the attribute will not be retrieved.  
  
### Return Value  
 Returns true if the `CSid` is found, false otherwise.  
  
### Remarks  
 Setting `pdwAttributes` to NULL provides a way of confirming the existence of the `CSid` without accessing the attribute. Note that this method should not be used to check access rights as incorrect results may occur under Windows 2000. Applications should instead use the [CAccessToken::CheckTokenMembership](../vs140/CAccessToken--CheckTokenMembership.md) method.  
  
##  <a name="ctokengroups__operator__eq"></a>  CTokenGroups::operator =  
 Assignment operator.  
  
```  
  
CTokenGroups & operator =(  
      const TOKEN_GROUPS &  rhs  
   ) throw(...);  
   CTokenGroups & operator =(  
      const CTokenGroups &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The `CTokenGroups` object or [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure to assign to the `CTokenGroups` object.  
  
### Return Value  
 Returns the updated `CTokenGroups` object.  
  
##  <a name="ctokengroups__operator_const_token_groups__star"></a>  CTokenGroups::operator const TOKEN_GROUPS *  
 Casts a value to a pointer to the **TOKEN_GROUPS** structure.  
  
```  
  
operator const TOKEN_GROUPS *( ) const throw(...);  
  
```  
  
### Remarks  
 Casts a value to a pointer to the [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure.  
  
## See Also  
 [Security Sample](../vs140/Visual-C---Samples.md)   
 [CSid Class](../vs140/CSid-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Security Global Functions](../vs140/Security-Global-Functions.md)