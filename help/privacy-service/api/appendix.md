---
keywords: Experience Platform;home;popular topics
solution: Experience Platform
title: Accepted identity namespaces and qualifiers
topic: developer guide
---

# Appendix

## Standard identity namespaces {#standard-namespaces}

All identities that are sent to Privacy Service must be provided under a specific identity namespace. Identity namespaces are a component of [Adobe Experience Platform Identity Service](../../identity-service/home.md) that indicate the context to which an identity relates.

The following table outlines several commonly used, pre-defined identity types made available by Experience Platform, along with their associated `namespace` values:

| Identity type | `namespace` | `namespaceId` |
| --- | --- | --- |
| Email | Email | 6 |
| Phone | Phone  | 7 |
| Adobe Advertising Cloud ID | AdCloud | 411 |
| Adobe Audience Manager UUID | CORE | 0 |
| Adobe Experience Cloud ID | ECID | 4 |
| Adobe Target ID | TNTID | 9 |
| Apple ID for Advertisers  | IDFA | 20915 |
| Google Ad ID  | GAID | 20914 |
| Windows AID  | WAID  | 8 |

>[!NOTE] Each identity type also has a `namespaceId` integer value, which can be used in place of the `namespace` string when setting the identity's `type` property to "namespaceId". See the section on [namespace qualifiers](#namespace-qualifiers) for more information.

You can retrieve a list of identity namespaces in use by your organization by making a GET request to the `idnamespace/identities` endpoint in the Identity Service API. See the [Identity Service developer guide](../../identity-service/api/getting-started.md) for more information.

## Namespace qualifiers

When specifying a `namespace` value in the Privacy Service API, a **namespace qualifier** must be included in a corresponding `type` parameter. The following table outlines the different accepted namespace qualifiers.

| Qualifier | Definition |
| --------- | ---------- |
| standard | One of the standard namespaces defined globally, not tied to an individual organization data set (for example, email, phone number, etc.). Namespace ID is provided. |
| custom | A unique namespace created in the context of an organization, not shared across the Experience Cloud. The value represents the friendly name ("name" field) to be searched for. Namespace ID is provided. |
| integrationCode | Integration code - similar to "custom", but specifically defined as the integration code of a datasource to be searched for. Namespace ID is provided. |
| namespaceId | Indicates the value is the actual ID of the namespace that was created or mapped through the namespace service. |
| unregistered | A freeform string that is not defined in the namespace service and is taken "as is". Any application that handles these kinds of namespaces checks against them and handle if appropriate for the company context and data set. No namespace ID is provided. |
| analytics | A custom namespace that is mapped internally in Analytics, not in the namespace service. This is passed in directly as specified by the original request, without a namespace ID |
| target | A custom namespace understood internally by Target, not in the namespace service. This is passed in directly as specified by the original request, without a namespace ID |

## Accepted product values

The following table outlines the accepted values for specifying an Adobe product in the `include` attribute of a job creation request.

Product | Value for use in the `include` attribute
--- | ---
Adobe Advertizing Cloud | "AdCloud"
Adobe Analytics | "Analytics"
Adobe Audience Manager | "AudienceManager"
Adobe Campaign | "Campaign"
Adobe Experience Platform | "aepDataLake"
Adobe Primetime Authentication | "primetimeAuthentication"
Adobe Target | "Target"
Customer Record Service | "CRS"
Real-time Customer Profile | "ProfileService"