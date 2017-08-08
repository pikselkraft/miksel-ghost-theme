# Miksel Theme

A minimalist, responsive theme focus on content for [Ghost](http://ghost.org) by [Pikselkraft](http://www.dereksalmon.me).

Last tested with Ghost v0.11.10

## Table of contents

* [Installation](##Installation)
* [Features](#features)
* [Configuring](#configuring)
* [License](#license)

## Installation
1. Download the files  and unzip it
2. You can make different customization (**you can find details about them in the section Configuration**)
 * Replace the `example` disqus_shortname with your shortname on *line 13* of **partials/custom/comments.hbs**, or delete the {{comments}} partials on post.hbs to remove comments altogether
 * Configure the follow buttons in **partials/custom/follow.hbs** (see section **Configuration**)
3. Add the folder to the **content/themes** directory of your Ghost installation
4. Restart Ghost and then go to Ghost's Settings (http://your.domain.com/ghost/settings/general/). Choose "Miksel" from the theme dropdown menu and save your changes.

##  Features
* Focused on content
* Mobile first and Fully responsive
* HTML5 semantics, WAI-ARIA and Rich Snippets roles (json)
* Ready for Ghost Latest Version
* Disqus comments integration
* Syntax Highlight with [Prism](http://prismjs.com/)
* Google Universal Analytics snippet
* OpenGraph and Twitter Cards meta's
* Baseline HTML5 features responsive meta
* One-file CSS for performance
* Based on flexbox and grid
* Minify css
* Typography Maniac
 * Scale typography
 * Responsive typography
* Ghost customization
 *  Tag Page Support
 *  Static Page Support
 * Post Sharing
 * Author Page
 * Next & Previous Post Navigation
* [Online Documentation](http://pixelcraft.work)


## Configuring
### Editing Follow Buttons and email
Miksel  is based on a custom icon set made in Fontello.
See the Font Awesome documentation for the [full list of icons](http://fortawesome.github.io/Font-Awesome/icons/). You can find the icon shortcut in `bundle.css`

You can customize the icons of the header in **custom/follow.hbs** file in `/partials/custom/follow.hbs`.

Make sure to replace the `username` in the URLs so the links point to your profiles. Or delete the useless profiles.

	If you want to add an email (it's better to hash it)
	<a href="mailto:you@example.com"><i class="icon-mail"></i></a>

### Comments
You can add your disqus URL  in **comments.hbs** file in `/partials/custom/comments.hbs`.

Delete {{> custom/comments}} in **post.hbs** if you don't use comment on your website.

### Email / contact
You can add your email with mailto  in **follow.hbs** file in `/partials/custom/follow.hbs`. It's better to hash it in order to avoid spam.

### meta.hbs
All configurable meta are located in `/partials/custom/meta.hbs`.

* Theme color on mobile
* Custom favicon (based on (favomatic generator)[http://www.favicomatic.com])
 * **favicon.ico is at the root of the folder**
* Windows application tiles

### Analytics
You can add google analytics code or another tracking tool with the code injection in Settings.

### Syntax Highlight
To add a syntax highlight, you must embed your code like this:

```language-markup
<p class="awesome">This HTML should be syntax highlighted</p>
```

```language-css
h1 {
font-family: 'montserratsemibold';
font-style: normal;
letter-spacing: 0em;font-size: 4.7rem;
}
```

Find more information for others languages: [Prism](http://prismjs.com/)

### Design
The CSS structure is based on BEM and atom design systems.
You can make modification directly in the bundle.min.css file or in the `assets/css/bundle.css` file.

### Typography and fonts

The fonts use in this webdesign are Noto and Montserrat from Google fonts.
There are used locally to avoid the dependencies to an external website.

You can change the fonts in the folder `assets/fonts`.

You will need to update `assets/js/font.js` file in order to match you new fonts. This script check your fonts and manage the fonts loading process.

Update the font names on *line 16, 17* . You can add or delete lines.

The current fonts of the theme:

	var fontA = new FontFaceObserver('Noto');
	var fontB = new FontFaceObserver('montserratsemibold');

You will need to update the @font-face in CSS too. You can update it in bundle.css.

## Credits / Ressources

* NPM
* PostCSS
* Ghost team
* Favomatic
* Font awesome et Fontello
* BEM CSS
* Atomic design
* Responsive typography
* Check the human.txt for personal thanks

## License
[MIT License](https://mit-license.org) © Pikselkraft
