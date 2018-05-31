---
Description: Most LSA Policy functions require a handle to the Policy object for the system to query or modify. To obtain a handle to a Policy object, call LsaOpenPolicy and specify the name of the system you want to access and the set of access permissions required.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Opening a Policy Object Handle
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Opening a Policy Object Handle

Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify. To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](https://msdn.microsoft.com/library/windows/desktop/aa378299) and specify the name of the system you want to access and the set of access permissions required.

The access permissions required for your application depend on the actions it performs. For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md#lsa-policy-functions).

If the call to [**LsaOpenPolicy**](https://msdn.microsoft.com/library/windows/desktop/aa378299) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system. Your application then passes this handle in subsequent LSA Policy function calls. When your application no longer needs the handle, it should call [**LsaClose**](/windows/win32/Ntsecapi/nf-ntsecapi-lsaclose?branch=master) to free it.

The following example shows how to open a [**Policy**](policy-object.md) object handle.


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&amp;ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &amp;lusSystemName,    //Name of the target system.
        &amp;ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &amp;lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-privilege-gly). For details about which permissions your application should request when calling [**LsaOpenPolicy**](https://msdn.microsoft.com/library/windows/desktop/aa378299), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.

To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/win32/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex?branch=master) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/win32/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname?branch=master) (to access an existing trusted domain). Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls. As with [**LsaOpenPolicy**](https://msdn.microsoft.com/library/windows/desktop/aa378299), your application should call [**LsaClose**](/windows/win32/Ntsecapi/nf-ntsecapi-lsaclose?branch=master) when it no longer needs the handle to the trusted domain's **Policy** object.

 

 


