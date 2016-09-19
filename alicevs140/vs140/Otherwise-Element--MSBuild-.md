---
title: "Otherwise Element (MSBuild)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de3997e9-1595-4263-a886-95530b56a319
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Otherwise Element (MSBuild)
Specifies the block of code to execute if and only if the conditions of all `When` elements evaluate to `false`.  
  
 <Project\>  
 <Choose\>  
 <When\>  
 <Choose\>  
 ...  
 <Otherwise\>  
 <Choose\>  
 ...  
  
## Syntax  
  
```  
<Otherwise>  
    <PropertyGroup>... </PropertyGroup>  
    <ItemGroup>... </ItemGroup>  
    <Choose>... </Choose>  
</Otherwise>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Choose](../vs140/Choose-Element--MSBuild-.md)|Optional element.<br /><br /> Evaluates child elements to select one section of code to execute. There may be zero or more `Choose` elements in an `Otherwise` element.|  
|[ItemGroup](../vs140/ItemGroup-Element--MSBuild-.md)|Optional element.<br /><br /> Contains a set of user-defined [Item](../vs140/Item-Element--MSBuild-.md) elements. There may be zero or more `ItemGroup` elements in an `Otherwise` element.|  
|[PropertyGroup](../vs140/PropertyGroup-Element--MSBuild-.md)|Optional element.<br /><br /> Contains a set of user-defined [Property](../vs140/Property-Element--MSBuild-.md) elements. There may be zero or more `PropertyGroup` elements in an `Otherwise` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Choose](../vs140/Choose-Element--MSBuild-.md)|Evaluates child elements to select one section of code to execute.|  
  
## Remarks  
 There may be only one `Otherwise` element in a `Choose` element, and it must be last element.  
  
 The `Choose`, `When`, and `Otherwise` elements are used together to provide a way to select one section of code to execute out of a number of possible alternatives. For more information, see [MSBuild Conditional Constructs](../vs140/MSBuild-Conditional-Constructs.md).  
  
## Example  
 The following project uses the `Choose` element to select which set of property values in the `When` elements to set. If the `Condition` attributes of both `When` elements evaluate to `false`, the property values in the `Otherwise` element are set.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <PropertyGroup>  
        <Configuration Condition="'$(Configuration)' == ''">Debug</Configuration>  
        <OutputType>Exe</OutputType>  
        <RootNamespace>ConsoleApplication1</RootNamespace>  
        <AssemblyName>ConsoleApplication1</AssemblyName>  
        <WarningLevel>4</WarningLevel>  
    </PropertyGroup>  
    <Choose>  
        <When Condition=" '$(Configuration)'=='debug' ">  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <DebugType>full</DebugType>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\Debug\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
            <ItemGroup>  
                <Compile Include="UnitTesting\*.cs" />  
                <Reference Include="NUnit.dll" />  
            </ItemGroup>  
        </When>  
        <When Condition=" '$(Configuration)'=='retail' ">  
            <PropertyGroup>  
                <DebugSymbols>false</DebugSymbols>  
                <Optimize>true</Optimize>  
                <OutputPath>.\bin\Release\</OutputPath>  
                <DefineConstants>TRACE</DefineConstants>  
            </PropertyGroup>  
        </When>  
        <Otherwise>  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\$(Configuration)\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
        </Otherwise>  
        </Choose>  
    <Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />  
</Project>  
```  
  
## See Also  
 [MSBuild Conditional Constructs](../vs140/MSBuild-Conditional-Constructs.md)   
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)