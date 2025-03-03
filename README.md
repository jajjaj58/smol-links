# Smol Links #
**Contributors:** [dphiffer](https://profiles.wordpress.org/dphiffer/)  
**Donate link:** https://themarkup.org/donate  
**Tags:** short url, shlink  
**Requires at least:** 4.5  
**Tested up to:** 6.0.0  
**Requires PHP:** 7.3  
**Stable tag:** 0.0.1  
**License:** GPLv2 or later  
**License URI:** https://www.gnu.org/licenses/gpl-2.0.html  

Create and manage Shlink short links from WordPress

## Description ##

__This plugin is a work in progress, development is ongoing.__

A WordPress dashboard interface for managing a self-hosted [Shlink URL shortener](https://shlink.io/) instance.

* Create and edit Shlinks short links from a manager interface
* Optionally generate new short URLs upon saving new posts
* Manage multiple short URL domains, with an assigned default
* Automatically tag each short link, configurable with a filter hook
* Customize long URLs automatically using a filter hook (e.g., to add query arguments)
* Integrates with [WordPress Sentry](https://wordpress.org/plugins/wp-sentry-integration/) plugin, if installed

__Filter hooks__

* `smol_links_tags` - assigns tags to each saved short link (default: `["smol-links-server:$hostname", "smol-links-user:$username"]`)
* `smol_links_long_url` - automatically adjust the long URL redirect
* `smol_links_manager_tabs` - customizes the manager tabs (array: ["Tab label" => [*Shlink API query*]])

# Developer setup #

__Developer dependencies:__

* [node.js](https://nodejs.org/) (tested on v16)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)

__Build and start:__

```
./bin/build.sh
./bin/start.sh
```

__Running tests:__

```
docker-compose exec web composer --working-dir="/var/www/html/wp-content/plugins/smol-links" test
```

## Installation ##

1. Upload `smol-links` folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Configure the __Smol Links__ settings from your WordPress dashboard

## Changelog ##

### 0.0.1 ###
* Generate short URLs upon saving a post
* Create/edit short URLs from a manager

## Upgrade Notice ##
