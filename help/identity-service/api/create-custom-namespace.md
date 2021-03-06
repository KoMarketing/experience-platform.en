---
keywords: Experience Platform;home;popular topics
solution: Experience Platform
title: Create a custom namespace
topic: API guide
---

# Creating a custom namespace

Using the [!DNL Identity Namespace] API, you can create a custom identity namespace that will be available only to your organization.

For recommendations around creating custom namespaces, see [the Identity Service FAQ documentation](../troubleshooting-guide.md).

>[!NOTE] Namespaces are a qualifier for identities. As such, once a namespace has been created, it cannot be deleted.

**API format**

```http
POST /idnamespace/identities
```

**Request**

```shell
curl -X POST \
  https://platform-va7.adobe.io/data/core/idnamespace/identities \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
        "name": "Loyalty Member",
        "code": "Loyalty",
        "description": "Loyalty Program Member ID",
        "idType": "Cross_device"
      }'
```

**Response**

```json
{
    "updateTime": 1576286879075,
    "code": "Loyalty",
    "status": "ACTIVE",
    "description": "Loyalty Program Member ID",
    "id": 10093197,
    "createTime": 1576286879075,
    "idType": "Cross_device",
    "name": "Loyalty Member",
    "custom": true
}
```

## Next steps

Proceed to the next tutorial to [list the native ID of an identity](./list-native-id.md)