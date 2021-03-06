<p align="center">
  <img src="https://avatars0.githubusercontent.com/u/1316274?v=3&s=200">
</p>

Translation Exchange Chef scripts for AWS
=====================

The scripts allow you to quickly launch new instances of WordPress on AWS using OpsWorks.

It will install the following components:

* Nginx
* php5-fpm
* MysQL 
* WordPress


Instructions
==================

1. Login to AWS and navigate to OpsWorks (https://console.aws.amazon.com/opsworks/home)
2. Click on "Add stack" and create a new stack using the following settings:

* Chef version: **11.10**
* Default operating system: **Ubuntu 14.04 LTS**
* Use custom Chef cookbooks: **Yes**
* Repository type: **Git**
* Repository URL: https://github.com/translationexchange/trex-chef.git
* Default root device type: **EBS backed**


3. Add a new layer using the following settings:

* Layer type: **Custom**

4. Modify the layer Recipes with the following values:

* Under Custom Chef Recipes, add the following recipe to the Setup phase:

  **drupal8-nginx-mysql56**

* Add the following package to be installed during setup:
 
  **php5-gd**

5. Add a new instance for the layer and launch it.

* Once the instance is up and running you can navigate to the instance's IP address and configure your WordPress.

6. Configure your WordPress database using the following information:

* Database name: drupal
* Username: drupaluser
* Password: bkW.2fNcaY#d99zpvnQhE8kqbncfg*qi9jBozt(aG


Once Drupal is configured, you can create your admin user and proceed with installing themes and plugins.

Good luck!


Links
==================

* Register at TranslationExchange.com: https://translationexchange.com

* Follow TranslationExchange on Twitter: https://twitter.com/translationx

* Connect with TranslationExchange on Facebook: https://www.facebook.com/translationexchange

* If you have any questions or suggestions, contact us: info@translationexchange.com


Copyright and license
==================

Copyright (c) 2017 Translation Exchange, Inc.

GNU General Public License, version 2

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

http://www.gnu.org/licenses/gpl-2.0.html
