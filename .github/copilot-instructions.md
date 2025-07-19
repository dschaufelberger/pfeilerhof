# GitHub Copilot Instructions
These instructions are designed to help you effectively use GitHub Copilot in your development workflow. Follow these guidelines to maximize your productivity and ensure a smooth coding experience.

## Jekyll and Best Practices

This repository uses [Jekyll](https://jekyllrb.com/) for static site generation. When using GitHub Copilot with Jekyll projects, keep these best practices in mind:

- Follow the existing folder structure for pages, layouts, includes, and assets.
- Use [Liquid](https://shopify.github.io/liquid/) templating syntax where appropriate.
- Keep content and layout concerns separated: use `_layouts` for templates, `_includes` for reusable snippets, and `assets` for static files.
- When adding or editing pages, use Markdown (`.md`) or HTML as appropriate, and include YAML front matter at the top of each page.
- When creating or editing SCSS files, always add empty YAML front matter (`---`) at the very top of main SCSS files to ensure Jekyll processes them correctly. Main SCSS files should be placed in the `Pfeilerhof/assets/css` directory.
- IMPORTANT! Test your changes locally with `bundle exec jekyll build` before committing.
- Avoid committing files in the `_site` directory; this folder is generated and should not be tracked.
- Document any custom plugins or configuration changes in the repository.
- Respect permalinks configured in the frontmatter of pages when creating new pages or modifying existing ones and when linking to pages within the site.

By following these practices, you help maintain a clean, organized, and functional Jekyll site.

## Project Directory Structure

The repository follows a standard Jekyll project structure. Key directories and their purposes:

- `_layouts/`: Page templates for different layouts.
- `_includes/`: Reusable HTML snippets (headers, footers, navigation, etc.).
- `_sass/`: Partial SCSS files for styles, imported into main SCSS files.
- `assets/`: Static files such as images, main SCSS and JS.
- `pages/`: Markdown or HTML files for site pages.
- `_site/`: Generated output (should not be committed).
- `Gemfile` & `Gemfile.lock`: Ruby dependencies for Jekyll and plugins.
- `_config.yml`: Main Jekyll configuration file.

Refer to this structure when adding or editing files to keep the project organized and maintainable.

## Technology

This project is built with Jekyll and leverages modern web standards:

- **HTML5**: Use semantic HTML5 elements and features wherever possible to ensure accessibility, SEO, and maintainability.
- **CSS**: Use the latest CSS features (such as custom properties, flexbox, grid, and modern selectors) to create responsive and maintainable layouts. SCSS is used for organization and maintainability.
- **Liquid**: Jekyll's templating language is used for dynamic content and layout logic.
- **SCSS**: Styles are written in SCSS for better organization and modularity. Use variables, mixins, and nesting to keep styles DRY (Don't Repeat Yourself).

When adding or editing code, prefer modern, standards-based approaches. Only use polyfills or workarounds if absolutely necessary for required browser support.

## Layout

All layouts should be designed to be responsive and mobile-first:

- Start with a layout optimized for small screens and progressively enhance for larger devices using media queries.
- Use CSS flexbox and grid for flexible, adaptive layouts.
- Ensure navigation, images, and text scale appropriately on all devices.
- Test changes on multiple screen sizes to guarantee usability and visual consistency.

Prioritize accessibility and performance in all layout decisions.

## Code Style
- Follow rules in the `.editorconfig` file for consistent coding styles across different editors.
- Add empty line between SCCS rules to improve readability.