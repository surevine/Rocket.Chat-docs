# Authentication

* [CAS](https://docs.rocket.chat/administrator-guides/authentication/cas/)
* [LDAP](https://docs.rocket.chat/administrator-guides/authentication/ldap/)
* [Oauth](https://docs.rocket.chat/administrator-guides/authentication/oauth/)
* [SAML](https://docs.rocket.chat/administrator-guides/authentication/saml/)
* [Wordpress](https://docs.rocket.chat/administrator-guides/authentication/wordpress/)

## External Authentication

If you need to automatically login users from your own website you can look at [Iframe integration page](../../developer-guides/iframe-integration/) or you can use the REST API [Login](../../developer-guides/rest-api/authentication/login.md) in combination with [deeplinking](../../developer-guides/deeplink.md) and the resumeToken.

```text
# get the resumeToken from your REST API login - it's the authToken field
https://yourown.rocket.chat/home?resumeToken=abcd123456789
```

