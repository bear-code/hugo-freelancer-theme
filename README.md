# Freelancer Theme

Freelancer Theme is a one page freelancer portfolio based on the [original Bootstrap theme](//github.com/IronSummitMedia/startbootstrap-freelancer) by [David Miller](//github.com/davidtmiller) and on [Jerome Lachaud](//github.com/jeromelachaud)'s [Jekyll theme](//github.com/jeromelachaud/freelancer-theme). This Hugo theme features several content sections, a responsive portfolio grid with hover effects, full page portfolio item modals and a contact form.

![Hugo Freelancer Theme screenshot](https://raw.githubusercontent.com/digitalcraftsman/hugo-freelancer-theme/master/images/screenshot.png)


## Contents

- [Installation](#installation)
- [Getting started](#getting-started)
    - [The config file](#the-config-file)
    - [Make the contact form working](#make-the-contact-form-working)
    - [Add social networks](#add-social-networks)
    - [Create your portfolio](#create-your-portfolio)
    - [Nearly finished](#nearly-finished)
- [Contributing](#contributing)
- [License](#license)
- [Annotations](#annotations)


## Installation

Inside the folder of your Hugo site run:

    $ mkdir themes
    $ cd themes
    $ git clone https://github.com/dhughesbc/hugo-freelancer-theme

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.


## Getting started

After installing the Freelancer Theme successfully it requires a just a few more steps to get your site running.


### The config file

Take a look inside the [`exampleSite`](//github.com/dhughesbc/hugo-freelancer-theme/tree/master/exampleSite) folder of this theme. You'll find a file called [`config.toml`](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/exampleSite/config.toml).
It contains detailed information about the setup of the contact form ([or see below](#make-the-contact-form-working)) and the customization of all strings in this theme. 

To use it, copy the [`config.toml`](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/exampleSite/config.toml) into the root folder of your Hugo site. Feel free to change strings as you like.


### Make the contact form working

Since this page will be static, you can use [formspree.io](//formspree.io/) as proxy to send the actual email. Each month, visitors can send you up to one thousand emails without incurring extra charges. Begin the setup by following the steps below:

1. Copy the [`contact-thank-you.md`](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/exampleSite/content/contact-thank-you.md) file into the content folder of your Hugo site. This needs to exist to build the page that users are redirected to 
after submitting the form to [formspree.io](//formspree.io/). The contents of this file are not used for anything.
2. Enter your email address under 'email' in the [`config.toml`](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/exampleSite/config.toml)
3. Upload the generated site to your server
4. Send a dummy email yourself to confirm your account
5. Click the confirm link in the email from [formspree.io](//formspree.io/)
6. You're done. Happy mailing!


### Add social networks

In the footer you can link some of your social network accounts. Search for `[params.footer.social.networks]` at the bottom of the file. The configuration should look similar to this one:

```toml
[[params.footer.social.networks]]
    icon = "fa-github"
    link = "//github.com/spf13/hugo"
```

The variable 'icon' represents the shown icon of the social network. It's a CSS class of Fontawesome's popular icon font. Search [here](//fortawesome.github.io/Font-Awesome/icons) if you need a particular icon.

### Create your portfolio

Beside the config file, there is in `data` another subfolder called [`projects`](//github.com/dhughesbc/hugo-freelancer-theme/tree/master/exampleSite/data/projects) which hosts the files that will appear as your projects in the portfolio section. Such a project file might look like [this one](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/exampleSite/data/projects/2014-07-13-project-1.yaml) written in YAML:

```yaml
modalID: 1
title: Project Cabin
img: cabin.png
clientLink: "http://an-awesome-site-i-built.com"
description: Use this area of the page to describe your project. The icon above is part of a free icon set by [Flat Icons](//sellfy.com/p/8Q9P/jV3VZ/"). On their website, you can download their free set with 16 icons, or you can purchase the entire set with 146 icons for only $12!
```

Copy the folder [`projects`](//github.com/dhughesbc/hugo-freelancer-theme/tree/master/exampleSite/data/projects) inside the `data` folder into the **root** directory of your site. Let's make some changes to show your work.

Pay attention to the `modalID`. It must be a unique integer and be incremented with each new project you want to add to the portfolio. Otherwise, the corresponding modal can't be rendered.

Furthermore, you can use Markdown syntax for URLs like here `[text](//url.to/source)` in the description. Copy the image of a project into `static/img/portfolio` and **just** enter the filename.


### Nearly finished

In order to see your site in action, run Hugo's built-in local server. 

    $ hugo server -w

Now enter `localhost:1313` in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/dhughesbc/hugo-freelancer-theme/issues) to let me know. Or make directly a [pull request](//github.com/dhughesbc/hugo-freelancer-theme/pulls).


## License

This theme is released under the Apache License 2.0 For more information read the [License](//github.com/dhughesbc/hugo-freelancer-theme/blob/master/LICENSE).


## Annotations

Thanks to [Steve Francia](//github.com/spf13) for creating Hugo and the awesome community around the project.
