## Obtain Token Request

### Structure

`ObtainTokenRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_id` | `String` |  | The Square-issued ID of your application, available from the [application dashboard](https://connect.squareup.com/apps). |
| `client_secret` | `String` |  | The Square-issued application secret for your application,<br>available from the [application dashboard](https://connect.squareup.com/apps). |
| `code` | `String` | Optional | The authorization code to exchange.<br>This is required if `grant_type` is set to `authorization_code`, to indicate that<br>the application wants to exchange an authorization code for an OAuth access token. |
| `redirect_uri` | `String` | Optional | The redirect URL assigned in the [application dashboard](https://connect.squareup.com/apps). |
| `grant_type` | `String` |  | Specifies the method to request an OAuth access token.<br>Valid values are: `authorization_code`, `refresh_token`, and `migration_token` |
| `refresh_token` | `String` | Optional | A valid refresh token for generating a new OAuth access token.<br>A valid refresh token is required if `grant_type` is set to `refresh_token` ,<br>to indicate the application wants a replacement for an expired OAuth access token. |
| `migration_token` | `String` | Optional | Legacy OAuth access token obtained using a Connect API version prior<br>to 2019-03-13. This parameter is required if `grant_type` is set to<br>`migration_token` to indicate that the application wants to get a replacement<br>OAuth access token. The response also returns a refresh token.<br>For more information, see [Migrate to Using Refresh Tokens](https://developer.squareup.com/docs/authz/oauth/migration). |

### Example (as JSON)

```json
{
  "client_id": "client_id8",
  "client_secret": "client_secret8",
  "code": null,
  "redirect_uri": null,
  "grant_type": "grant_type4",
  "refresh_token": null,
  "migration_token": null
}
```

