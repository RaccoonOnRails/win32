---
Description: Implements the IX509PrivateKey and IX509PublicKey interfaces.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Private and Public Key Functions
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Private and Public Key Functions

CertEnroll.dll implements the [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) and [**IX509PublicKey**](/windows/win32/CertEnroll/nn-certenroll-ix509publickey?branch=master) interfaces. You can, for example, use the [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) interface to perform the following actions on a [*private key*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-private-key-gly):

-   Create, open, close, import, export, and delete the key.
-   Specify or retrieve the [*public key algorithm*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-public-key-algorithm-gly).
-   Specify or retrieve information about the available [*cryptographic service provider*](https://msdn.microsoft.com/library/windows/desktop/ms721572#-security-cryptographic-service-provider-gly) (CSP) that support the public key algorithm.
-   Specify or retrieve the [*certificate*](https://msdn.microsoft.com/library/windows/desktop/ms721572#-security-certificate-gly) associated with the [*private key*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-private-key-gly).
-   Specify or retrieve the name of the [*key container*](https://msdn.microsoft.com/library/windows/desktop/ms721590#-security-key-container-gly).
-   Specify or retrieve a description of and a display name for the key.
-   Specify or retrieve the export constraints places on a private key.
-   Specify or retrieve a Boolean value that indicates whether the key exists.
-   Specify or retrieve a value that indicates how the key is protected before use.
-   Specify or retrieve a value that indicates whether the key can be used for signing, encryption, or both.
-   Specify or retrieve a value that identifies the specific purpose for which the key can be used.
-   Specify or retrieve the length of the key.
-   Specify or retrieve a value that indicates whether the key is used or saved in the context of a computer or user.
-   Retrieve a Boolean value that specifies whether the key has been opened.
-   Specify a personal identification number to access a private key on a [*smart card*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-smart-card-gly).
-   Specify or retrieve the name of the CSP associated with the key.
-   Specify or retrieve the [*security descriptor*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-security-descriptor-gly) for the key.

Each of the following sections identifies a function exported by Xenroll.dll that can be used to manage a [*cryptographic key*](https://msdn.microsoft.com/library/windows/desktop/ms721572#-security-cryptographic-key-gly). Each topic also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists:

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Related topics](#related-topics)

## ContainerNameWStr

The [**ContainerNameWStr**](https://msdn.microsoft.com/library/windows/desktop/aa385533) function in Xenroll.dll specifies or retrieves the name of the [*key container*](https://msdn.microsoft.com/library/windows/desktop/ms721590#-security-key-container-gly).

When using CertEnroll.dll, you can perform the following actions to retrieve the name of a key container:

1.  Call the [**Request**](/windows/win32/CertEnroll/nf-certenroll-ix509enrollment-get_request?branch=master) property on an existing [**IX509Enrollment**](/windows/win32/CertEnroll/nn-certenroll-ix509enrollment?branch=master) object.
2.  Call the [**GetInnerRequest**](/windows/win32/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest?branch=master) method on the request returned from step 1 to retrieve the innermost request.
3.  Call **QueryInterface** on the [**IX509CertificateRequest**](/windows/win32/CertEnroll/nn-certenroll-ix509certificaterequest?branch=master) object returned from step 2 to cast to an [**IX509CertificateRequestPkcs10**](/windows/win32/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10?branch=master) object.
4.  Call the [**PrivateKey**](https://msdn.microsoft.com/library/windows/desktop/aa387352) property on the PKCS \#10 request.
5.  Call the [**ContainerName**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-get_containername?branch=master) property on the [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) object retrieved from step 4.

## GenKeyFlags

The [**GenKeyFlags**](https://msdn.microsoft.com/library/windows/desktop/aa385573) function defined in Xenroll.dll specifies or retrieves flags used to generate a private key or [*public/private key pair*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-public-private-key-pair-gly).

When using CertEnroll.dll, you can specify a number of different properties that will determine how a private key is created. For more information, see [**Create**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-create?branch=master).

## GetKeyLen

The [**GetKeyLen**](https://msdn.microsoft.com/library/windows/desktop/aa385593) function defined in Xenroll.dll retrieves the maximum or minimum key size of an encryption key.

When using CertEnroll.dll, you can call the [**Length**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-get_length?branch=master) property on an [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) or [**IX509PublicKey**](/windows/win32/CertEnroll/nn-certenroll-ix509publickey?branch=master) object to retrieve the key size, in bits.

## GetKeyLenEx

The [**GetKeyLenEx**](https://msdn.microsoft.com/library/windows/desktop/aa385595) function defined in Xenroll.dll retrieves the maximum or minimum key size or the increment length of an encryption key.

When using CertEnroll.dll, you can call the [**Length**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-get_length?branch=master) property on an [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) or [**IX509PublicKey**](/windows/win32/CertEnroll/nn-certenroll-ix509publickey?branch=master) object to retrieve the key size, in bits. If an algorithm supports incremental key lengths, you can call the [**IncrementLength**](/windows/win32/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength?branch=master) property on the [**ICspAlgorithm**](/windows/win32/CertEnroll/nn-certenroll-icspalgorithm?branch=master) object to retrieve the increment value. You can also call the [**MinLength**](/windows/win32/CertEnroll/nf-certenroll-icspalgorithm-get_minlength?branch=master) and [**MaxLength**](/windows/win32/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength?branch=master) properties to retrieve the minimum and maximum key sizes.

## GetSupportedKeySpec

The [**GetSupportedKeySpec**](https://msdn.microsoft.com/library/windows/desktop/aa385615) function defined in Xenroll.dll retrieves a value that indicates whether a CSP supports exchange keys, signing keys, or both.

When using CertEnroll.dll, you can call the [**KeySpec**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec?branch=master) property on the [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) or [**ICspInformation**](/windows/win32/CertEnroll/nn-certenroll-icspinformation?branch=master) objects to retrieve the operations supported by the key.

## KeySpec

The [**KeySpec**](https://msdn.microsoft.com/library/windows/desktop/aa385639) function defined in Xenroll.dll specifies or retrieves the key type.

When using CertEnroll.dll, you can call the [**KeySpec**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec?branch=master) property on an [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) object to retrieve the operations supported by the key.

## LimitExchangeKeyToEncipherment

The [**LimitExchangeKeyToEncipherment**](https://msdn.microsoft.com/library/windows/desktop/aa385642) function defined in Xenroll.dll specifies or retrieves a Boolean value that indicates whether an encryption key can be used only for data or key encipherment.

CertEnroll.dll does not contain a direct equivalent for this function. You can, however, achieve a nearly equivalent result by specifying an [**IX509ExtensionKeyUsage**](/windows/win32/CertEnroll/nn-certenroll-ix509extensionkeyusage?branch=master) object and adding it to the certificate request.

## PVKFileNameWStr

The [**PVKFileNameWStr**](https://msdn.microsoft.com/library/windows/desktop/aa385664) function defined in Xenroll.dll specifies or retrieves the name of a file that contains exported keys.

When using CertEnroll.dll, you can call the [**Export**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-export?branch=master) method on an [**IX509PrivateKey**](/windows/win32/CertEnroll/nn-certenroll-ix509privatekey?branch=master) object to export a key to a **BSTR**. You can call the [**ExportPublicKey**](/windows/win32/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey?branch=master) method to export the [*public key*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-public-key-gly) portion of an asymmetric key pair.

## ReuseHardwareKeyIfUnableToGenNew

The [**ReuseHardwareKeyIfUnableToGenNew**](https://msdn.microsoft.com/library/windows/desktop/aa385698) function defined in Xenroll.dll specifies or retrieves a Boolean value that indicates whether an existing key is reused when an error is encountered when generating a new key.

When using CertEnroll.dll, you can call the [**InitializeFromCertificate**](/windows/win32/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate?branch=master) method on an [**IX509CertificateRequestPkcs10**](/windows/win32/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10?branch=master) object and specify a value of the [**X509RequestInheritOptions**](/windows/win32/CertEnroll/ne-certenroll-x509requestinheritoptions?branch=master) enumeration type to reuse an existing private key.

## UseExistingKeySet

The [**UseExistingKeySet**](https://msdn.microsoft.com/library/windows/desktop/aa386150) function defined in Xenroll.dll specifies or retrieves a Boolean value that indicates whether to use existing keys.

When using CertEnroll.dll, you can call the [**InitializeFromCertificate**](/windows/win32/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate?branch=master) method on an [**IX509CertificateRequestPkcs10**](/windows/win32/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10?branch=master) object and specify a value of the [**X509RequestInheritOptions**](/windows/win32/CertEnroll/ne-certenroll-x509requestinheritoptions?branch=master) enumeration type to reuse existing private and public keys.

## Related topics

<dl> <dt>

[Mapping Xenroll.dll to CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 


