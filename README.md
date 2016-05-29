Jumbotron Child Theme
=====================

This is a basic child theme for the Jumbotron theme for Phire CMS 2
to demonstrate extending an existing theme. It is to be used with the
phire-theme module. It is built using the Bootstrap Jumbotron component,
along with a few other Bootstrap components.

OVERVIEW
========

Child themes are the preferred way to extend and edit an existing theme
without changing anything in the original parent theme. That way, if the
parent theme is updated by the system, any changes and upgrades you've made
to your child theme should remain largely intact.

INSTALLATION & USE
==================

Any child theme is installed by copying the child theme files next to the
parent theme and naming the folder the same as the parent theme, but with
the additional "-child" suffix. For example:

* ./jumbotron-theme-1.0
* ./jumbotron-theme-1.0-child

The themes module will auto-detect the child theme and ask you to install it,
which will then register it with the system. From there, you'll be able to
select the available templates from the parent and child themes, and edit
the templates and code of the child theme as needed.

For a child theme to be correctly parsed and installed with the system, it
expects there to minimally be at least one style sheet file with a doc-block
containing the following identification:

For example, at the top of a "styles.css" file:

```css
/**
 * Theme Name: My Cool Child Theme
 * Author: My Name
 * Description: This is a my cool child theme for Phire CMS 2
 * Version: 1.0
 */
```

PARENT THEME REFERENCE
======================

If you need to reference files and assets of the parent theme, the variable
`$parentThemePath` is available in the child theme's scope, for example:

```php
<?php include $parentThemePath . '/inc/header.phtml'; ?>
```
