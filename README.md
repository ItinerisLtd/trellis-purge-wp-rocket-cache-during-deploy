# trellis-purge-kiwp-rocketache-during-deploy

[![GitHub tag](https://img.shields.io/github/tag/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy/tags)
[![license](https://img.shields.io/github/license/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy/blob/master/LICENSE)

Purge [WP Rocket](https://wp-rocket.me/) cache when [Trellis](https://github.com/roots/trellis) deploys [Bedrock](https://github.com/roots/bedrock).

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Requirements](#requirements)
- [Installation](#installation)
- [Role Variables](#role-variables)
- [Usage](#usage)
- [FAQs](#faqs)
  - [Does it trigger cache preload after purge?](#does-it-trigger-cache-preload-after-purge)
  - [Can I use it together with `trellis-purge-kinsta-cache-during-deploy`?](#can-i-use-it-together-with-trellis-purge-kinsta-cache-during-deploy)
  - [It looks awesome. Where can I find some more goodies like this?](#it-looks-awesome-where-can-i-find-some-more-goodies-like-this)
  - [This package isn't on wp.org. Where can I give a ⭐️⭐️⭐️⭐️⭐️ review?](#this-package-isnt-on-wporg-where-can-i-give-a-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F-review)
- [Testing](#testing)
  - [Syntax Check](#syntax-check)
- [Author Information](#author-information)
- [Feedback](#feedback)
- [Change log](#change-log)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Requirements

- Trellis [411981f](https://github.com/roots/trellis/commit/411981fb4a7ef9be079f50fbf317db9fc290e91b) or later
- Ansible v2.6 or later
- [WP Rocket](https://wp-rocket.me/)

## Installation

Add this role to `requirements.yml`:
```yaml
# requirements.yml
- src: https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy
  version: 0.1.0 # Check for latest version!
```

Run the command:
```bash
➜ ansible-galaxy install -r requirements.yml --force
```

## Role Variables

Add this role to the [`deploy_after` hook](https://roots.io/trellis/docs/deploys/#hooks):
```yaml
# group_vars/all/deploy-hooks.yml
# Learn more on https://roots.io/trellis/docs/deploys/#hooks
deploy_after:
  - "{{ playbook_dir }}/vendor/roles/trellis-purge-wp-rocket-cache-during-deploy/tasks/main.yml"
```

## Usage

[Deploy](https://roots.io/trellis/docs/deploys/#example) as usual. No special action needed.

## FAQs

### Does it trigger cache preload after purge?

Yes if you enabled [cache preload](https://docs.wp-rocket.me/article/8-how-the-cache-is-preloaded).

### Can I use it together with `trellis-purge-kinsta-cache-during-deploy`?

Yes, this role is compatible with [trellis-purge-kinsta-cache-during-deploy](https://github.com/ItinerisLtd/trellis-purge-kinsta-cache-during-deploy).

### It looks awesome. Where can I find some more goodies like this?

- Articles on [Itineris' blog](https://www.itineris.co.uk/blog/)
- More projects on [Itineris' GitHub profile](https://github.com/itinerisltd)
- Follow [@itineris_ltd](https://twitter.com/itineris_ltd) and [@TangRufus](https://twitter.com/tangrufus) on Twitter
- Hire [Itineris](https://www.itineris.co.uk/services/) to build your next awesome site

### This package isn't on wp.org. Where can I give a ⭐️⭐️⭐️⭐️⭐️ review?

Thanks! Glad you like it. It's important to make my boss know somebody is using this project. Instead of giving reviews on wp.org, consider:

- tweet something good with mentioning [@itineris_ltd](https://twitter.com/itineris_ltd)
- star this [Github repo](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy)
- watch this [Github repo](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy)
- write blog posts
- submit pull requests
- [hire Itineris](https://www.itineris.co.uk/services/)

## Testing

### Syntax Check

```bash
➜ ansible-playbook -i 'localhost,' --syntax-check tests/test.yml
```

## Author Information

[trellis-purge-wp-rocket-cache-during-deploy](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy) is a [Itineris Limited](https://www.itineris.co.uk/) project created by [Tang Rufus](https://typist.tech).

Special thanks to [the Roots team](https://roots.io/about/) whose [Trellis](https://github.com/roots/trellis) make this project possible.

Full list of contributors can be found [here](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy/graphs/contributors).

## Feedback

**Please provide feedback!** We want to make this library useful in as many projects as possible.
Please submit an [issue](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy/issues/new) and point out what you do and don't like, or fork the project and make suggestions.
**No issue is too small.**

## Change log

Please see [CHANGELOG](./CHANGELOG.md) for more information on what has changed recently.

## License

[trellis-purge-wp-rocket-cache-during-deploy](https://github.com/ItinerisLtd/trellis-purge-wp-rocket-cache-during-deploy) is released under the [MIT License](https://opensource.org/licenses/MIT).
