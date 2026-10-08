
# Migrating from 3.3.7 to 3.4.0

## Enum technical values cleanup

We removed `*Unrecognized` and `*Unspecified` values from all enumerations.
These were technical values for internal use.

For a limited number of enums where the Chromium counterpart has an unknown
state, we added `Unknown` values:

- `PermissionType.Unknown`
- `CreditCardNetwork.Unknown`
- `RequestStatus.Unknown`
- `NetError.Unknown`
- `SuggestionsPopupType.Unknown`
- `ColorModel.Unknown`
- `DuplexMode.Unknown`

Where applicable, replace removed values with the new `Unknown` value.

## Removed `NetError` values

We removed certain `NetError` enum values that no longer exist in Chromium. 
If your code references any of these values, you will see compilation errors indicating which specific
values are no longer available:

* `NoSslVersionsEnabled`
* `HttpsProxyTunnelResponse`
* `SslHandshakeNotCompleted`
* `SslBadPeerPublicKey`
* `SynReplyNotReceived`
* `EncodingConversionFailed`
* `UnrecognizedFtpDirectoryListingFormat`
