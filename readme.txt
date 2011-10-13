=== Gravity Forms Salesforce Add-on ===
Tags: gravity forms, forms, gravity, form, crm, gravity form, salesforce, salesforce plugin, form, forms, gravity, gravity form, gravity forms, secure form, simplemodal contact form, wp contact form, widget, sales force, customer, contact, contacts, address, addresses, address book
Requires at least: 2.8
Tested up to: 3.2.1
Stable tag: trunk
Contributors: katzwebdesign
Donate link:https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=zackkatz%40gmail%2ecom&item_name=Gravity%20Forms%20Salesforce%20Addon&no_shipping=0&no_note=1&tax=0&currency_code=USD&lc=US&bn=PP%2dDonationsBF&charset=UTF%2d8

Integrate the remarkable <a href="http://wordpressformplugin.com/?r=salesforce" rel="nofollow">Gravity Forms</a> plugin with Salesforce.

== Description ==

> This plugin requires the amazing <a href="http://wordpressformplugin.com/?r=salesforce" rel="nofollow">Gravity Forms plugin</a>. <strong>Don't use Gravity Forms? <a href="http://wordpressformplugin.com/?r=salesforce" rel="nofollow">Get the plugin</a></strong>, then start using this great plugin!

### Integrate Gravity Forms with Salesforce
Add one setting, check a box when configuring your forms, and all your form entries will be added to Salesforce from now on. <strong>Integrating with Salesforce has never been so simple.</strong>

###Gravity Forms + Salesforce = A Powerful Combination

This free Salesforce Add-On for Gravity Forms adds contacts into Salesforce automatically, making customer relationship management simple. The setup process takes less than three minutes, and your contact form will be linked with Salesforce.

#### Now with Custom Field support! ####
<a href="http://wordpress.org/extend/plugins/gravity-forms-salesforce/faq/">Read the FAQ</a> for information on how to integrate with Custom Fields.

#### Other Gravity Forms Add-ons:

* <a href="http://wordpress.org/extend/plugins/gravity-forms-highrise/">Gravity Forms Highrise Add-on</a> - Integrate Gravity Forms with Highrise, a CRM
* <a href="http://wordpress.org/extend/plugins/gravity-forms-addons/">Gravity Forms Directory & Addons</a> - Turn Gravity Forms into a WordPress Directory plugin.
* <a href="http://wordpress.org/extend/plugins/gravity-forms-constant-contact/">Gravity Forms + Constant Contact</a> - If you use Constant Contact and Gravity Forms, this plugin is for you.
* <a href="http://wordpress.org/extend/plugins/gravity-forms-exacttarget/">Gravity Forms ExactTarget Add-on</a> - Integrate Gravity Forms with ExactTarget

If you have questions, comments, or issues with this plugin, <strong>please leave your feedback on the <a href="http://wordpress.org/tags/gravity-forms-salesforce?forum_id=10">Plugin Support Forum</a></strong>.

== Screenshots ==

1. The Gravity Forms Salesforce Add-on settings page
2. It's easy to integrate Gravity Forms with Salesforce: check a box in the "Advanced" tab of a form's Form Settings

== Installation == 

1. Upload plugin files to your plugins folder, or install using WordPress' built-in Add New Plugin installer
1. Activate the plugin
1. Go to the plugin settings page (under Forms > Salesforce)
1. Enter the information requested by the plugin.
1. Click Save Settings.
1. If the settings are correct, it will say so.
1. Follow on-screen instructions for integrating with Salesforce.

== Frequently Asked Questions == 

= How do I set a custom Lead Source? =
This feature support was added in version 1.1.1. `gf_salesforce_lead_source` is the filter.

Add the following to your theme's `functions.php` file. Modify as you see fit:

`
add_filter('gf_salesforce_lead_source', 'make_my_own_lead_source', 1, 3); 

function make_my_own_lead_source($lead_source, $form_meta, $data) {
	// $lead_source - What was about to be used (normally Gravity Forms Form Title)
	// $form_meta - Gravity Forms form details
	// $data - The data passed to Salesforce

	return $lead_source; // Return something else if you want to.
}
`

= Can I use Salesforce Custom Fields? =

With version 1.1, you can. When you are trying to map a custom field, you need to set either the "Admin Label" for the input (in the Advanced tab of each field in the  Gravity Forms form editor) or the Parameter Name (in Advanced tab, visible after checking "Allow field to be populated dynamically") to be the API Name of the Custom Field as shown in Salesforce. For example, a Custom Field with a Field Label "Web Source" could have an API Name of `SFGA__Web_Source__c`.

You can find your Custom Fields under [Your Name] &rarr; Setup &rarr; Leads &rarr; Fields, then at the bottom of the page, there's a list of "Lead Custom Fields & Relationships". This is where you will find the "API Name" to use in the Admin Label or Parameter Name.

= Does this plugin require Gravity Forms? =
This plugin requires the brilliant [Gravity Forms plugin](http://wordpressformplugin.com/?r=salesforce). __Don't use Gravity Forms? [Buy the plugin](http://wordpressformplugin.com/?r=salesforce)__ and start using this add-on plugin!

= What's the license for this plugin? =
This plugin is released under a GPL license.

== Changelog ==

= 1.1.1 = 
* Fixes issue where all forms get submitted to Salesforce, not only enabled forms (<a href="http://www.seodenver.com/forums/topic/all-forms-posting-to-saleforce/">reported on support forum</a>).
* Added a new filter to modify the lead source `gf_salesforce_lead_source`, <a href="http://wordpress.org/support/topic/657400" rel="nofollow">as requested here</a>. Passes three arguments: `$lead_source`, `$gf_form_meta`, `$salesforce_data`.

= 1.1 =
* Added support for Custom Fields (view the FAQ here, or the Gravity Forms Salesforce Add-on Settings page for this plugin)
* Improved authentication check in the settings page - no longer creates a blank lead.
* Fixed some PHP notices

= 1.0 =
* Launch!

== Upgrade Notice ==

= 1.1.1 = 
* Fixes issue where all forms get submitted to Salesforce, not only enabled forms (<a href="http://www.seodenver.com/forums/topic/all-forms-posting-to-saleforce/">reported on support forum</a>).
* Added a new filter to modify the lead source `gf_salesforce_lead_source`, <a href="http://wordpress.org/support/topic/657400" rel="nofollow">as requested here</a>. Passes three arguments: `$lead_source`, `$gf_form_meta`, `$salesforce_data`.

= 1.1 =
* Added support for Custom Fields (view the FAQ here, or the Gravity Forms Salesforce Add-on Settings page for this plugin)
* Improved authentication check in the settings page - no longer creates a blank lead.
* Fixed some PHP notices

= 1.0 =
* Launch!