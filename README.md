# <div align="left"><img src="https://rapids.ai/assets/images/rapids_logo.png" width="90px"/> &nbsp; [RAPIDS.ai](https://rapids.ai.com) Website

Code and content for the [RAPIDS.ai](https://rapids.ai) static public website. This is a refactor from the previous Jekyll backed version to use the [Hugo](https://gohugo.io/about/) static site framework and the [Bulma](https://bulma.io/) css framework. On occasion it uses [Apline.js](https://alpinejs.dev/start-here).


## Design and Layout
Use the [Template Design Guide](template.html) and [RAPIDS Brand Guide](brand.html) for reference with starting new pages.

Refer to the [Bulma Documentation](https://bulma.io/documentation/) for reference to the CSS class names and components. Note: many CSS classes are overwritten through `custom.css`.
- [Column System](https://bulma.io/documentation/columns/basics/)
- [Container Class](https://bulma.io/documentation/layout/container/)
- [Spacing, Margin, and Padding Helpers](https://bulma.io/documentation/helpers/spacing-helpers/)

Hugo uses templates, layouts, and directories to build pages. The `/layouts/_defaults` folder contains `Baseof.html` for the root page chrome layout, followed by `section.html` for directory `_index.html` files, then `single.html` for sub pages. The `/layout/index.html` page is for the `/content/_index.html` page only, but still uses `Baseof.html` for chrome. Note: `partials` can only be used as part of template `layouts`, and `shortcodes` can only be used as part of `content` sections/pages. All in all, more complicated than it needs to be...


## Requirements
The site required Hugo in order to be built. Follow the [Hugo documentation](https://gohugo.io/about/) for assistance.

All logos and images are located in the [images](/static/images) folder. Externally (no website) referenced files should be placed in the [assets](/assets) folder.

Font Icons are used from [Font Awesome](https://fontawesome.com/), and include Pro account icons.

In the future it will employ the more optimized assets and hugo pipe features.

## Hosting, Development and Previews
After installing Hugo, run `hugo server` to see a developer preview and `hugo` to build for production. You can also preview pages locally from the `/public` dir after building, but may need to use `python -m http.server` or similar for all functionality.

Hosting is currently done through [Netlify](https://www.netlify.com/), which should create a preview when PRs are pushed to the main repository. 

