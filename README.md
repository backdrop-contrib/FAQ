# FAQ

The Frequently Asked Questions (faq) module allows users with the 'administer
faq' permission to create question and answer pairs which they want displayed on
the 'faq-page' page.  The 'faq-page' page is automatically generated from the
FAQ nodes configured and the layout of this page can be modified on the settings
page. Users will need the 'view faq page' permission to view the 'faq-page'
page.

An alternative to the built-in 'faq-page' is to use one of the example Views
layouts provided which you can easily customise to your needs using the Views
UI. Note, the configuration settings for the module do not apply to the Views
layouts.

## Installation

1. Install this module using the official Backdrop CMS instructions at
<https://backdropcms.org/guide/modules>.
2. Enable permissions at admin/people/permissions.
3. Configure the module at admin/config/content/faq - not used for Views
   layouts.
4. You can use the default faq page at "faq-page" or enable one of the page
   layouts in the example Views.  For the Views pages you can change the url if
   needed, but if you wish to change the url for the built-in page (faq-page)
   you need to create a url alias at admin/config/search/path.

## Upgrade notice

When using categorized FAQ nodes, the disabling of the FAQ module causes the
vocabulary to lose the association with the FAQ content type. This results in no
FAQ nodes being displayed when you re-enable the FAQ module. Before opening an
issue, please verify that this setting is still in place.

## Configuration

Once the module is activated, you can create your question and answer pairs by
creating FAQ nodes (Create content >> FAQ).  This allows you to edit the
question and answer text.  In addition, if the 'Taxonomy' module is enabled and
there are some terms configured for the FAQ node type, it will also be possible
to put the questions into different categories when editing.

## Known issues

### No FAQs appear after module upgrade

When using categorized FAQ nodes, the disabling of the FAQ module causes the
vocabulary to lose the association with the FAQ content type. This results in no
FAQ nodes being displayed when you re-enable the FAQ module. Before opening an
issue, please verify that this setting is still in place.

### `<p>` tags appear in FAQ question text

When using CKEditor, `<p>` and other HTML tags may appear in the displayed
question text. This is because the faq title or question input box is a textarea
and not a textfield, so the faq module can accommodate longer question texts.
The p-tags come from the editor used and not the FAQ module. This is because the
editors attach themselves to all textareas on a given page.  Details on how to
prevent this can be found at http://drupal.org/node/294708

### Clicking on category links takes user to front page

Instead of being taken to the categorized faq page, the front page is displayed
when the user clicks on a faq category. This is something to do with the
path module and can be easily fixed by doing a bulk update of paths for the
faq vocabulary.

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.

## Maintainers

* [herbdool](https://github.com/herbdool)
* Seeking co-maintainers.

## Credits

Ported to Backdrop by [herbdool](https://github.com/herbdool).

This module is based on the 7.x-1.x branch for Drupal,
originally written and maintained by:

* [Stella Power](http://drupal.org/user/66894)
* [vijaycs85](https://www.drupal.org/u/vijaycs85)
* [mohammed-j-razem](https://www.drupal.org/u/mohammed-j-razem)
* [andreytroeglazov](https://www.drupal.org/u/andreytroeglazov)
* [nancydru](https://www.drupal.org/u/nancydru)
