# Maulana Kurniawan's Portfolio

Forked from:

[![Particle](https://github-readme-stats.vercel.app/api/pin/?username=nrandecker&repo=particle&show_owner=true&theme=vue#gh-light-mode-only)](https://github.com/nrandecker/particle#gh-light-mode-only)
[![Particle](https://github-readme-stats.vercel.app/api/pin/?username=nrandecker&repo=particle&show_owner=true&theme=vue-dark#gh-dark-mode-only)](https://github.com/nrandecker/particle#gh-dark-mode-only)

Added with my own customizations & features!

## Basic Setup

1. Download latest version of Ruby.
    - Windows:
        - Download and install [Ruby+Devkit](https://rubyinstaller.org/downloads/) and just proceed, left all the options as-is in the installer.
        - After installation is completed, open `cmd.exe` and run:

            ```bash
            ridk install
            ```

        - Complete the configuration.
    - Debian, Ubuntu and their derivatives:
        - Install Ruby and other prerequisites:

            ```bash
            sudo apt-get install ruby-full build-essential zlib1g-dev
            ```

        - Set up a gems installation directory for your user account.

            ```bash
            echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
            echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
            echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
            source ~/.bashrc
            ```

    - Other Linux: Refer to [this guide](https://jekyllrb.com/docs/installation/other-linux/).
    - macOS: I don't know, never use macOS. Refer to [this guide](https://jekyllrb.com/docs/installation/macos/) for macOS.
2. Install Jekyll and Bundler:

    ```bash
    gem install jekyll bundler
    ```

3. Clone this repository:

    ```bash
    git clone https://github.com/maulana-kurniawan/maulana-kurniawan.github.io.git
    ```

## Site and User Settings

Fill in your informations on the `_config.yml` and `_data.yml` file to customize and personalize your site.

**Don't forget to change your url before you deploy your site!**

## Color and Particle Customizations

1. Color & font customization:
    - Edit the `_fonts.scss` inside `_sass` directory for font source, either from Google Fonts or local fonts.
    - Edit `_vars.scss` inside `_sass` directory for  set the color and font variable values.
2. Particle customization:
    - Go to [particle.js](https://vincentgarreau.com/particles.js/) site configuring the `particle.js`.
    - After finishing up the configuration, tap the **"→ Download current config (json)"** button, `particlesjs-config.json` will be downloaded and place it in this project root directory.

## Customize the Favicon

The favicons are located in the `assets/img/favicons/` directory. Replace them with your own.

### Generate the favicon

Prepare a square image (PNG, JPG, or SVG) with a size of 512x512 or more, and then go to the online tool [Real Favicon Generator](https://realfavicongenerator.net/) and click the `Select your Favicon image` to upload your image file.

In the next step, the webpage will show all usage scenarios. You can keep the default options, scroll to the bottom of the page, and click the `Generate your Favicons and HTML code` button to generate the favicon.

### Download & Replace

Download the generated package, unzip and delete the following two from the extracted files:

- `browserconfig.xml`
- `site.webmanifest`

And then copy the remaining image files (`.png` and `.ico`) to cover the original files in the directory assets/img/favicons/ of your Jekyll site. If your Jekyll site doesn’t have this directory yet, just create one.

The following table will help you understand the changes to the favicon files:

| File(s) |  From Online Tool  | From Local  |
|  :---:  |        :---:       |    :---:    |
| `*.png` | :heavy_check_mark: |     :x:     |
| `*.ico` | :heavy_check_mark: |     :x:     |

> :heavy_check_mark: means keep, :x: means delete.

**Thanks to [Chirpy](https://chirpy.cotes.page/posts/customize-the-favicon/) for the "*Customize the Favicon*" guide!**

## Test and run the site in local

In order to compile the assets and run Jekyll on local you need to follow this steps:

- Install gem dependencies by running:

    ```bash
    bundle install
    ```

- Build the site and make it available on a local server with live reload to changes made:

    ```bash
    bundle exec jekyll s -l
    ```

## License

This theme is free and open source software, distributed under the The MIT License. So feel free to use this Jekyll theme anyway you want.

## Credits

This theme was partially designed with the inspiration from these fine folks and of course, author of this repo upstream:

- [Willian Justen](https://github.com/willianjusten/will-jekyll-template/)
- [Vincent Garreau](https://github.com/VincentGarreau/particles.js/)
- [Nathan Randecker](https://github.com/nrandecker/particles/)
