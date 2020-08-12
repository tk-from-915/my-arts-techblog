=== Attachment Importer ===
Contributors: piontkowski
Tags: importer, import, attachment, attachments, image, images, wordpress, wxr, xml
Requires at least: 3.0
Tested up to: 4.0
Stable tag: 0.6.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Import attachments from another WordPress blog using a WXR file.

== Description ==

= What is this? =

I found the WordPress Importer plugin is good for importing posts and comments, but is lacking when it comes to importing large attachments (like images) from large sites. My import would often time out and crash. I wrote this plugin to help with my own blog migrations, but I hope you find it useful too.

= Usage =

0. As a prerequisite, import your WXR file using the WordPress importer, but do not select the option to Download and Import Attachments. I have found that an import file up to 15MB big will work as long as you don't import attachments.
1. Navigate to the Attachment Importer screen.
2. Select your WXR export file.
3. Select the user you would like to be the owner of the downloaded images. Default: current user.
4. Sit back and let the importer run. The process can take as little as 10 seconds for 10 images, or about two hours for 2000 images. These times depend on the server that hosts your WordPress site.
5. If you receive any errors during the process, try running the file again after it finishes.  The plugin is programmed to ignore files that match the following criteria:
   * Same name
   * Same file name
   * Same upload date
   * Same file size

= How it works. =

This plugin uses [FileReader](https://developer.mozilla.org/en-US/docs/Web/API/FileReader) and to parse the XML file in the browser, then uses ajax to request WordPress perform individual uploads. 

= License =

Attachment Importer - A plugin for WordPress to import attachments from another blog using a WXR file.
Copyright (C) 2014 Toasted Lime

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

The license and copyright applies to all resources bundled with this plugin, except as noted below:

Portions of this plugin use code from:

* [WordPress Importer](http://wordpress.org/extend/plugins/wordpress-importer/) which is distributed under the terms of the GNU GPL v2, Copyright (C) 2013 wordpressdotorg.
* [jQuery UI Smoothness Theme](http://jqueryui.com/themeroller/) which is distributed under the terms of MIT License, Copyright (C) 2014 jQuery Foundation and other contributors.

== Installation ==

1. Either a) download from the WordPress plugin repository, or b) upload the attachment-importer directory to your plugins directory.
2. Navigate to Plugins -> Attachment Importer and activate.
3. Go to Tools -> Import -> Attachment Importer to run.

== Changeset ==

= 0.6.0 =
Should not get "Remote server did not respond" as often.

= 0.5.6 =

* Invalid file type produces non-fatal error.

= 0.5.5 =

* Added an overall progress bar.
* Improve how the program responds to events like fatal errors, AJAX failure, or if there are no attachments in the import file.

= 0.5.4 =

* Fixed issue reading namespaces in import file that caused the program not to work in FireFox and Internet Explorer.
* Moved plugin to Import menu from the Media menu.

= 0.5.3 =

* Added option to add five second delay between image ajax requests
* Reformat Readme
* Added jQuery tooltip

