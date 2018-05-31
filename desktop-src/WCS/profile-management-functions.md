---
title: Profile Management Functions
description: Profile Management Functions
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS),functions
- WCS (Windows Color System),functions
- image color management,functions
- color management,functions
- colors,functions
- WCS reference,functions
- reference for WCS,functions
- Windows Color System (WCS),profiles
- WCS (Windows Color System),profiles
- image color management,profiles
- color management,profiles
- colors,profiles
- WCS reference,profiles
- reference for WCS,profiles
- profile management
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Profile Management Functions

## Profile Management Functions

The following API functions are useful in profile management.



| Function                                                                               | Description                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDevice**](associatecolorprofilewithdevice.md)             | Associates a color profile with a device.                                                                                                            |
| [**CreateProfileFromLogColorSpace**](createprofilefromlogcolorspace.md)               | Converts a [**LOGCOLORSPACE**](/windows/win32/Wingdi/ns-wingdi-taglogcolorspacea?branch=master) to a device profile.                                                                               |
| [**DisassociateColorProfileFromDevice**](disassociatecolorprofilefromdevice.md)       | Disassociates a color profile from a device.                                                                                                         |
| [**EnumColorProfiles**](enumcolorprofiles.md)                                         | Enumerates color profiles that satisfy specified criteria.                                                                                           |
| [**GetColorDirectory**](getcolordirectory.md)                                         | Identifies the system color directory.                                                                                                               |
| [**GetDeviceGammaRamp**](/windows/win32/Wingdi/nf-wingdi-getdevicegammaramp?branch=master)                                       | Gets the gamma ramp from direct color display boards.                                                                                                |
| [**GetStandardColorSpaceProfile**](getstandardcolorspaceprofile.md)                   | Retrieves a registered standard space profile.                                                                                                       |
| [**InstallColorProfile**](installcolorprofile.md)                                     | Installs a color profile for use in the system.                                                                                                      |
| [**RegisterCMM**](registercmm.md)                                                     | Registers a CMM for use by the system. Used to install new CMMs.                                                                                     |
| [**SetDeviceGammaRamp**](/windows/win32/Wingdi/nf-wingdi-setdevicegammaramp?branch=master)                                       | Sets the gamma ramp on direct color display boards.                                                                                                  |
| [**SetStandardColorSpaceProfile**](setstandardcolorspaceprofile.md)                   | Registers a profile for a standard color space.                                                                                                      |
| [**UninstallColorProfile**](uninstallcolorprofile.md)                                 | Uninstalls a color profile from the system.                                                                                                          |
| [**UnregisterCMM**](unregistercmm.md)                                                 | Removes the CMM registration. Used to uninstall CMMs.                                                                                                |
| [**WcsAssociateColorProfileWithDevice**](wcsassociatecolorprofilewithdevice.md)       | Associates a specified WCS color profile with a specified device.                                                                                    |
| [**WcsCreateIccProfile**](wcscreateiccprofile.md)                                     | Converts a WCS profile into an ICC profile.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](wcsdisassociatecolorprofilefromdevice.md) | Disassociates a specified WCS color profile with a specified device on a specified computer.                                                         |
| [**WcsEnumColorProfiles**](wcsenumcolorprofiles.md)                                   | Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.                                       |
| [**WcsEnumColorProfilesSize**](wcsenumcolorprofilessize.md)                           | Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](wcsenumcolorprofiles.md) function to enumerate color profiles. |
| [**WcsGetDefaultColorProfile**](wcsgetdefaultcolorprofile.md)                         | Retrieves the default color profile for a device, or the device-independent default if the device is not specified.                                  |
| [**WcsGetDefaultColorProfileSize**](wcsgetdefaultcolorprofilesize.md)                 | Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.                                       |
| [**WcsGetDefaultRenderingIntent**](wcsgetdefaultrenderingintent.md)                   | Retrieves the default rendering intent in the specified profile management scope.                                                                    |
| [**WcsGetUsePerUserProfiles**](wcsgetuseperuserprofiles.md)                           | Determines whether the user has chosen to use a per-user profile association list for the specified device.                                          |
| [**WcsOpenColorProfile**](wcsopencolorprofile.md)                                     | Creates a handle to a specified color profile.                                                                                                       |
| [**WcsSetDefaultColorProfile**](wcssetdefaultcolorprofile.md)                         | Sets the default color profile name of the specified profile type in the specified profile management scope.                                         |
| [**WcsSetDefaultRenderingIntent**](wcssetdefaultrenderingintent.md)                   | Sets the default rendering intent in the specified profile management scope.                                                                         |
| [**WcsSetUsePerUserProfiles**](wcssetuseperuserprofiles.md)                           | Allows the user to specify whether to use a per-user profile association list for the specified device.                                              |



 

## Profile Consumption Functions

The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.

 

## Profiles and Profile Management Functions

The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.

Profiles contain information used by color processing algorithms to translate color between different color spaces. Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.

Profile management provides the following set of functionalities:

 

1. Installing color profiles for use in the system.

 

2. Associating one or more installed color profiles with any particular device.

 

3. Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing. This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.

 

4. Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.

The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.

 

**Per-user profile management and enabling execution in LUA context**

The goal of the design described in the current document is as follows:

 

1. Legacy ICM2 implementation does not provide support for per-user profile management. Different users cannot have their own profile settings. In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.

 

2. All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges. In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings. In WCS profile management, all per-user profile settings are configurable in LUA context. Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.

Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:

 

1. It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.

 

2. Installing a profile remains system wide and requires administrator privileges. This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.

 

Whether devices can be installed from LUA context is particular to what is supported for that class of device. For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies. Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.

 

3. Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges. Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.

Profile management scope indicates the scope of the operations performed; either per-user or system wide.

For each operation, it is indicated whether it can be done from LUA context. If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied. Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.



Operation

Profile Management Scope

Pre-condition

Post-condition

Executable in LUA context

${ROWSPAN2}$Install profile${REMOVE}$  

System wide

Profile copied, installed into the system, and available for use. Profile is enumerable in system-wide and current-user scope for all users.

During device driver installation, governed by driver installation policies. No, otherwise.

Current user

Not supported

${ROWSPAN2}$Uninstall profile${REMOVE}$  

System wide

Profile is installed in the system

Profile uninstalled from the system and optionally deleted from the profile store. Profile is no longer available for use and is not enumerable in any scope.

No

Current user

Not supported

${ROWSPAN2}$Associate profile with device${REMOVE}$  

System wide

Profile is installed and is of type ICC or CDMP

Profile is available for use with the device by all users. It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.

No

Current user

Profile is installed. It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.

Profile is available for use with the device by current user. It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.

Yes

${ROWSPAN2}$Disassociate profile from device${REMOVE}$  

System wide

Profile is associated with the device in system-wide scope and is of type ICC or CDMP

Profile is no longer available for use (except for users who have this association in their current-user scope as well). It is not enumerable in system-wide scope. It could be enumerable in current-user scope though, for a user who has this association in its scope.

No

Current user

Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.

Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).

Yes

${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$  

System wide

Profile is of type ICC or CDMP

The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope. (The profile is installed and associated to the device system wide, if that is not already the case.)

No

Current user

Profile is of type ICC or CDMP

The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this. (The profile is installed and associated to the device for current user, if that is not already the case.)

Yes, if the profile is already installed

${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$  

System wide

Only ICC and CDMP profiles can be associated with devices.

The profile is used by default for the particular type. Users can override this setting in the current-user scope. (The profile is installed, if that is not already the case.)

No

Current user

Only ICC and CDMP profiles can be associated with devices.

The profile is used by default for the particular type for current user. (The profile is installed, if that is not already the case.)

Yes, if the profile is already installed.

${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$  

System wide

Not applicable

Current user

Even for current-user queries on default profile settings, system-wide settings are returned for use.

Yes

${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$  

System wide

Only ICC and CDMP profiles can be associated with and enumerated for devices.

Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.

Yes

Current user

Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.

Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.

Yes

${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$  

System wide

Only ICC and CDMP profiles can be associated with and enumerated for devices.

Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.

Yes

Current user

Only ICC and CDMP profiles can be associated with and enumerated for devices.

Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.

Yes



 

The valid color profile types are provided by the COLORPROFILETYPE enumeration.

The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.

The valid profile type/subtype combinations are shown in the following table.



COLORPROFILETYPE

Valid COLORPROFILESUBTYPE

Notes

Device Default

Global Default

Intended Use

Intended Use

CPT\_ICC

CPST\_NONE

Get/Set default ICC profile associated with a device

CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace

Get/Set ICC profile as global RGB or custom working space profile. See Note.

The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive. The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.

CPT\_DMP

CPST\_NONE

Get/Set default DMP profile associated with a device

CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace

Get/Set DMP profile as global RGB or custom working space profile. See Note.

The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive. The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.



 

> [!Note]  
> When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.
>
>  
>
> When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.

 

The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.

### Profile management public API layer

Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user. ? Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call. o ICM2 APIs that work on current-user scope ? This is for operations that are supported for both system wide and current-user scope in WCS profile management. Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user. This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context. o ICM2 APIs that work on system-wide scope ? This is for operations (install profiles and uninstall profiles) that support only system-wide scope. No new WCS profile management APIs are created and existing APIs can be modified.

The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities. They are either device specific or global (device independent) settings. o Device specific configuration data: ? List of profiles associated with a particular device. ? Default profile for different profile types associated with a device. ? Matching mode of profiles used for enumeration. o Global configuration data: ? List of profiles installed in the system. ? Global default profile for different profile types. ? The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user. This is different from profile management scope. An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present. ? The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope. The storage layer is transparent to profile management scope. The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller. This logic is present in the ICM2/WCS API layer.

### Device-specific storage layer

The storage for different classes of devices like print, capture or display could be different from each other. For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection. ? This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.

The following diagram illustrates this architecture.



Profile Management Public API Layer

${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory). They call the configuration storage layer with appropriate storage scope.${REMOVE}$  

Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory). They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.

New WCS API with system-wide and current-user profile management scope support. They call the configuration storage layer with appropriate storage scope.



 



Profile Management Configuration Storage Layer

Device-independent global configuration routines

Device-specific configuration routines

${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$  

Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.

Device-Specific Storage layer

Print specific storage

Display specific storage

Capture specific storage



 

Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior. Install and uninstall operations fall in this category.

Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings. All operations other than install and uninstall fall in this category.

 

 



