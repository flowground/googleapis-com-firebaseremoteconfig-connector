# ![LOGO](logo.png) Firebase Remote Config **flow**ground Connector

## Description

A generated **flow**ground connector for the Firebase Remote Config API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/firebaseremoteconfig/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:22+03:00

## API Description

Firebase Remote Config API allows the 3P clients to manage Remote Config conditions and parameters for Firebase applications.

## Authorization

This API does not require authorization.

## Actions

### Get the latest version Remote Configuration for a project.<br/>
> Returns the RemoteConfig as the payload, and also the eTag as a<br/>
> response header.

*Tags:* `projects`

#### Input Parameters
* `project` - _required_ - The GMP project identifier. Required.
See note at the beginning of this file regarding project ids.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `bearer_token` - _optional_ - OAuth bearer token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Update a RemoteConfig. We treat this as an always-existing<br/>
> resource (when it is not found in our data store, we treat it as version<br/>
> 0, a template with zero conditions and zero parameters). Hence there are<br/>
> no Create or Delete operations. Returns the updated template when<br/>
> successful (and the updated eTag as a response header), or an error if<br/>
> things go wrong.<br/>
> Possible error messages:<br/>
> * VALIDATION_ERROR (HTTP status 400) with additional details if the<br/>
> template being passed in can not be validated.<br/>
> * AUTHENTICATION_ERROR (HTTP status 401) if the request can not be<br/>
> authenticate (e.g. no access token, or invalid access token).<br/>
> * AUTHORIZATION_ERROR (HTTP status 403) if the request can not be<br/>
> authorized (e.g. the user has no access to the specified project id).<br/>
> * VERSION_MISMATCH (HTTP status 412) when trying to update when the<br/>
> expected eTag (passed in via the "If-match" header) is not specified, or<br/>
> is specified but does does not match the current eTag.<br/>
> * Internal error (HTTP status 500) for Database problems or other internal<br/>
> errors.

*Tags:* `projects`

#### Input Parameters
* `project` - _required_ - The GMP project identifier. Required.
See note at the beginning of this file regarding project ids.
* `validateOnly` - _optional_ - Optional. Defaults to <code>false</code> (UpdateRemoteConfig call should
update the backend if there are no validation/interal errors). May be set
to <code>true</code> to indicate that, should no validation errors occur,
the call should return a "200 OK" instead of performing the update. Note
that other error messages (500 Internal Error, 412 Version Mismatch, etc)
may still result after flipping to <code>false</code>, even if getting a
"200 OK" when calling with <code>true</code>.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `bearer_token` - _optional_ - OAuth bearer token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-firebaseremoteconfig-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
