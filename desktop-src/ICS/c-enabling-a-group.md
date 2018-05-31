---
title: Enabling a Group
description: This example enables a group using the Windows Firewall with Advanced Security APIs.C++/\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ ++ Copyright (C) Microsoft.
ms.assetid: 098c5e88-848a-455b-8107-86dd72880ff4
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Enabling a Group

This example enables a group using the Windows Firewall with Advanced Security APIs.


```C++
/********************************************************************++
Copyright (C) Microsoft. All Rights Reserved.

Abstract:
    This C++ file includes sample code for enabling Windows Firewall
    exception groups using the Microsoft Windows Firewall APIs.

--********************************************************************/

#include <windows.h>
#include <stdio.h>
#include <netfw.h>

#pragma comment( lib, "ole32.lib" )
#pragma comment( lib, "oleaut32.lib" )


// Forward declarations
HRESULT     WFCOMInitialize(INetFwPolicy2** ppNetFwPolicy2);


int __cdecl main()
{
    HRESULT hrComInit = S_OK;
    HRESULT hr = S_OK;

    INetFwPolicy2 *pNetFwPolicy2 = NULL;

    // Rule group to use
    BSTR bstrRuleGroup = SysAllocString(L"File and Printer Sharing");
    VARIANT_BOOL bIsEnabled = FALSE;

    // Initialize COM.
    hrComInit = CoInitializeEx(
                    0,
                    COINIT_APARTMENTTHREADED
                    );

    // Ignore RPC_E_CHANGED_MODE; this just means that COM has already been
    // initialized with a different mode. Since we don't care what the mode is,
    // we'll just use the existing mode.
    if (hrComInit != RPC_E_CHANGED_MODE)
    {
        if (FAILED(hrComInit))
        {
            printf("CoInitializeEx failed: 0x%08lx\n", hrComInit);
            goto Cleanup;
        }
    }

    // Retrieve INetFwPolicy2
    hr = WFCOMInitialize(&amp;pNetFwPolicy2);
    if (FAILED(hr))
    {
        goto Cleanup;
    }

    // Check if the rule group is enabled for the Private profile
    hr = pNetFwPolicy2->IsRuleGroupEnabled(NET_FW_PROFILE2_PRIVATE, bstrRuleGroup, &amp;bIsEnabled);
    if (FAILED(hr))
    {
        printf("IsRuleGroupEnabled failed: 0x%08lx\n", hr);
        goto Cleanup;
    }

    if(!bIsEnabled)
    {
        // Group is not enabled for the Private profile - need to enable it
        printf("Rule Group is NOT enabled for the Private profile. Calling EnableRuleGroup...");

        hr = pNetFwPolicy2->EnableRuleGroup(NET_FW_PROFILE2_PRIVATE, bstrRuleGroup, TRUE);
        if (FAILED(hr))
        {
            printf("EnableRuleGroup failed: 0x%08lx\n", hr);
            goto Cleanup;
        }
    }
    else
    {
        printf("Rule Group is enabled for the Private profile");
    }

Cleanup:

    // Free BSTR's
    SysFreeString(bstrRuleGroup);

    // Release INetFwPolicy2
    if (pNetFwPolicy2 != NULL)
    {
        pNetFwPolicy2->Release();
    }

    // Uninitialize COM.
    if (SUCCEEDED(hrComInit))
    {
        CoUninitialize();
    }
   
    return 0;
}


// Instantiate INetFwPolicy2
HRESULT WFCOMInitialize(INetFwPolicy2** ppNetFwPolicy2)
{
    HRESULT hr = S_OK;

    hr = CoCreateInstance(
        __uuidof(NetFwPolicy2), 
        NULL, 
        CLSCTX_INPROC_SERVER, 
        __uuidof(INetFwPolicy2), 
        (void**)ppNetFwPolicy2);

    if (FAILED(hr))
    {
        printf("CoCreateInstance for INetFwPolicy2 failed: 0x%08lx\n", hr);
        goto Cleanup;        
    }

Cleanup:
    return hr;
}

```



 

 



