=== Place Login ===
Contributors: lebasca
Donate link: http://boroniatechnologies.com/contribute
Tags: login, sidebar, widget, place login, button login, form, register
Requires at least: 3.6
Tested up to: 4.4
Stable tag: 1.1.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Add a login widget in your sidebar or login button in any part of your page.

== Description ==

Place Login is a WordPress plugin that offers the same functionalities like most login widgets but it has default pages for Registration and Lost Password actions. 

Also, you can use a template tag to create a login button instead of using the login widget. 

= Translators =

* Spanish (es_ES) - [Catherine Lebastard](http://www.boroniatechnologies.com/)
* Serbian (sr_RS) - [Borisa Djuraskovi​c](http://www.webhostinghub.com/)

If you have created your own language pack, or have an update of an existing one, you can contact [me](http://boroniatechnologies.com/contact/) so that I can bundle it into Column Posts. You can download the latest [POT file](http://plugins.svn.wordpress.org/column-posts/trunk/languages/column-posts.pot).

== Installation ==

= Automatic installation =

  1. Go to the Dashboard and click Plugins > Add New.
  2. Enter Place Login under search textbox.
  3. Click Install Now to install this plugin.
  4. Confirm the popup window to install the plugin.
  5. Click Proceed to continue with the installation.
  6. Click Activate Plugin to activate it.

= Manual installation =

  1. Download the files for this plugin.
  2. Upload the files to the wp-content/plugins directory.
  3. Go to the Dashboard and find this plugin in the list.
  4. Click Activate Plugin to activate it.

The settings page is found in settings > Place Login.

== Frequently asked questions ==

= I have a “Page not found” message when I use the link to the default pages. =

Go to the Settings of the plugin, you can change the parent page under login links and Save it. If it still doesn’t work, you can go to Setting/Permalinks and click Save Changes.

= Can I use the WordPress login page instead of the plugin default pages? =

Yes, you have to enter the urls in the register and lost password fields under “Login links” section. These are the links for the following options:
– Registration: [blog site address]/wp-login.php?action=register
– Lost Password: [blog site address]/wp-login.php?action=lostpassword

= How can I use the WordPress profile page? =

You can add the link code in the links fields under “Logged in links” section. This is how the link code should be written:
<a href="[blog site address]/wp-admin/profile.php">Profile</a>

= How can I change the theme for the login button and login modal form? =

Open the functions.php file located in your WordPress theme and add this code:
add_action( 'wp_enqueue_scripts', 'login_theme', 9);

function login_theme(){
    wp_enqueue_style( 'jquery-ui', '[url address of the jquery theme]', false );
}

Note: The url address of the jquery theme can be located in your wordpress theme or hosted in Google. For example: I want to use the UI lightness jquery theme hosted in Google. So, I will replace [url address of the jquery theme] with https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.21/themes/ui-lightness/jquery-ui.css in the code above.

= Is it compatible with WordPress multisite? =

Yes, this plugin has been tested in Wordpres multisite. Also, it checks that only users assigned to the current site can have access to it.

Note: This plugin doesn’t validate the user email during the registration in Worpress multisite as well as regular WordPress.

= Where are the options of my user account? I can see only my user name and the avatar. =

Your user account options are shown when you move the pointer over the user name. A drop-down menu will appear below the user name with a list of link options.

= Can I have the sidebar in the plugin default pages when I use twenty ten theme? =

Yes, you have to copy the template directory of this plugin in your WordPress theme directory. After that, you can modify the template as you want but you shouldn’t delete the function that calls the form.

== Screenshots ==

1. Place Login Setting Options.
2. Place Login is displayed in the user account.
3. Place Login widget.
4. Place Login as a button.

== Changelog ==
= 1.1.2 =
* Update readme.txt

= 1.1.1 =
* Fixed the translation of this plugin

= 1.1 =
* Fixed type %USERNAME% and %USERID%

= 1.0.1 =
* Plugin version updated

= 1.0 =
* Plugin launched