# yii2-postmark-mailer

A eartotheground Postmark Yii2 component, including a catch to prevent sending emails to real email addresses when not on the Production environment

## Example config

```
return [
	'name' => 'APP_NAME',
	'language' => 'en-GB',
	'sourceLanguage' => 'en-GB',
	'timeZone' => 'UTC',
	'vendorPath' => dirname(dirname(__DIR__)) . '/vendor',
	'bootstrap' => ['log'],
	'aliases' => [
        '@bower' => '@vendor/bower-asset',
        '@npm'   => '@vendor/npm-asset',
    ],
	'components' => [
	    'db' => [
	    	...
	    ],
		'custommailer' => [
			'class' => 'eartotheground\yii2-postmark-mailer\PostmarkMailer',
			'postmarkServerToken' => 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX',
			'errorEmailAddress' => 'error-reporting-address@eartotheground.software',
			'safeEmailAddress' => 'local-and-qa-emails-address@eartotheground.software',
		],
```