Opauth-Facebook
=============
[Opauth][1] strategy for [Facebook](https://aapks.com/apk/facebook/) authentication.

Implemented based on https://developers.facebook.com/docs/authentication/

Getting started
----------------
1. Install Opauth-Facebook:
   ```bash
   cd path_to_opauth/Strategy
   git clone https://github.com/opauth/facebook.git Facebook
   ```
   or
   ```
   composer require opauth/facebook
   ```

2. Create Facebook application at https://developers.facebook.com/apps/
   - Remember to enter App Domains
   - "Website with Facebook Login" must be checked, but for "Site URL", you can enter any landing URL.

3. Configure Opauth-Facebook strategy with at least `App ID` and `App Secret`.

4. Direct user to `http://path_to_opauth/facebook` to authenticate

Strategy configuration
----------------------

Required parameters:

```php
<?php
'Facebook' => array(
	'app_id' => 'YOUR APP ID',
	'app_secret' => 'YOUR APP SECRET'
)
```

Even though `fields` is an optional configuration parameter for Opauth-Facebook, for most cases you would like to explicitly define it. It should be defined in a comma-separated string. 

Refer to [Facebook Fields Reference](https://developers.facebook.com/docs/graph-api/reference/user) for list of valid fields.

License
---------
Opauth-Facebook is MIT Licensed  
Copyright © 2012 U-Zyn Chua (http://uzyn.com)

[1]: https://github.com/opauth/opauth
