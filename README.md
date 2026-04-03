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

For local preview on this machine, use `bin/preview` and open `http://127.0.0.1:4000`. This uses the repo's `Gemfile.preview` and leaves the production GitHub Pages dependency stack in `Gemfile` untouched.

If you need to install the local preview gems first, run:

```bash
CPLUS_INCLUDE_PATH="$(xcrun --show-sdk-path)/usr/include/c++/v1" \
MAKE='make CXX=clang++' \
BUNDLE_GEMFILE=Gemfile.preview \
bundle install
```

The older GitHub Pages gem stack in `Gemfile` is still the production source of truth for deployment. The preview setup only exists to make local development smoother on modern macOS/Ruby toolchains.
