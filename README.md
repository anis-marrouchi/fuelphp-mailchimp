fuel-mailchimp
==============


Overview
=============================================
We needed mailchimp for tweetstrap.com (not available) to handle our newsletter related stuff, so i have decided to create this fuel package and share it on github.
The project will be based on a PHP 5.2+ API client for [v2 of the MailChimp API](http://apidocs.mailchimp.com/api/2.0/).
Installing the package
==================================
**The fuel way**

- run php oil package install fuelphp-mailchimp (you will need to add my git to your sources in your package cofiguration file: make a copy of the package configuration file located @ `\home\fuelphp\fuel\core\config\package.php` into your `\home\fuelphp\fuel\app\config\package.php`, then add `github.com/anis-marrouchi` to sources
- Rename fuelphp-mailchimp folder located @ `fuel/packages/` to mailchimp 

**The github way**

1. Clone (`git clone git://github.com/anis-marrouchi/fuelphp-mailchimp`) / [download](https://github.com/anis-marrouchi/fuelphp-mailchimp/archive/master.zip)
2. Rename folder to mailchimp and place in `fuel/packages/`

Configuration
==================================
1. Edit `fuel/packages/mailchimp/config/mailchimp.php` by adding your Mailchimp api
2. Add 'mailchimp' to the `'always_load/packages'` array in `app/config/config.php`. You can also call Fuel::add_package('mailchimp') whenever you need it).
3. Have fun :)

Getting started
=========================

A basic example: Retrieving all of the lists defined for your user account
> `function action_welcome()  
> {  
>   $mailchimp = new Mailchimp();  
> 	$lists = $mailchimp->lists->getList();  
> }`

More examples
=========================
Read and follow the api documentation located in the `docs` folder.

Support us
=============================================
*Support us by giving a **Star** to our project: **[twittstrap](https://github.com/twittstrap/twittstrap)**.*

A special thanks to the guys at [fuelphp](http://fuelphp.com/contribute/donate).
