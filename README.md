Taxonomy-meta-fields-plugin-for-Wordpress
=========================================

Plugin to manage and use custom meta fields within builtin and custom taxonomies

Category Meta plugin
=========================================
Contributors: Bas Matthee (v1.3), josecoelho, Randy Hoyt, steveclarkcouk, Vitaliy Kukin, Eric Le Bail, Tom Ransom

Update Log
=========================================
1.3   : Added WYSIWYG Editor support. Code refacturing and cleanup. Fixed bug with non-sanitized formfield names. Some minor bugfixing. CSS-file removed. User interface changed.

1.2.8 : Add Brazilian Portuguesetranslation thanks to josecoelho

1.2.7 : Small fix to make the image fields work in WordPress 3.4.

1.2.6 : Fix bug introduced in 1.2.5, allowing images to be inserted into posts again.

1.2.5 : Small fix to make the image fields work in WordPress 3.3.1.

1.2.4 : Small fix to make the meta list appear in the taxonomy edit page with WP3.0.1. && WP3.0.4 (thanks to webgrafia).

1.2.3 : Add a new meta type "check-box" with meta_value of "checked" when the box is checked (thanks to Joseph).

1.2.2 : Small fix to make the meta list appear in the taxonomy edit page with WP3.0.1. && WP3.0.4 (thanks to Patrick).

1.2.1 : Small fix to avoid problem wih global variables in the taxonomy list with WP3.0.1. (thanks to Jeff).

1.2.0 : Major release. Add the terms meta administration form on all terms (category / Tags / custom taxonomies) for WP version 3.0 and above.

1.1.1 : Fix a typo error when no meta has been configured.

1.1.0 : Major release. Test and debug to be fully compatible with version 3.0.x . Add the new "image" type for meta.

1.0.3 : Fix an error on the meta update method thanks to Tom Ransom for sending the fix.

1.0.2 : Debug when no meta is set.

1.0.1 : Add the possibility to replace special chars into meta name in the meta creation form in the option page.

1.0.0 : Add the option page to easily configure the meta list

0.0.1 : plugin initial creation.

Installation
=========================================

1. Unzip into your `/wp-content/plugins/` directory. If you're uploading it make sure to upload
the top-level folder. Don't just upload all the php files and put them in `/wp-content/plugins/`.
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Go to your Administration interface in the "Settings" menu a new "Category Meta" page is created.
Configure the meta you want to use.
4. go to your Administration interface, in the "Category" menu -> new fields are displayed in the category modification form with the meta you configured.
5. That's it!
6. you can use the folowing functions into your templates to retreive 1 meta:
`
if (function_exists('get_terms_meta'))
{
    $metaValue = get_terms_meta($category_id, $meta_key);
}
`
7. you can use the folowing functions into your templates to retreive all meta:
`
if (function_exists('get_all_terms_meta'))
{
    $metaList = get_all_terms_meta($category_id);
}
`