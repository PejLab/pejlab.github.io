# pejlab.org
 Website for the PejLab

## How to update the website

This site uses [Jekyll](https://jekyllrb.com/) to compile the markdown content and other files into html. The site is hosted on [GitHub Pages](https://pages.github.com/). To update the site, you need to clone the repository, make changes, and push the changes to the repository. You can also submit a pull request if you don't have write access to the repository. GitHub will automatically compile the site and make the changes live.

- Images and CSS files are in the `assets` folder.
- Basic site info is in `_config.yml`.
  - This includes the list of header items, which can either be a link to a page or an external link, e.g. to Google Scholar or GitHub. I customized `_includes/header.html` to allow for external links with a `title` and a `url`.
- The lab member info is in `_data/members.yml`.
  - The `image` field should be the filename of the image in `assets/images/people`.
  - Any formatting, links, etc. in the `bio` field should be in HTML, not markdown.
- The alumni info is in `_data/alumni.yml`.
  - Currently photos are not included for alumni, and bios should only include their current job.

After making changes, you can test the site locally by running `bundle exec jekyll serve` and going to `localhost:4000` in a web browser. You will need to have Ruby and Jekyll installed. See [here](https://jekyllrb.com/docs/installation/) for instructions. This compiles the site into `_site` and serves it locally. That folder will not be pushed to the repository, and only the source files are used to compile the site on GitHub Pages.
