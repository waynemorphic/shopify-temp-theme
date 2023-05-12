## EXPERIMENTAL SHOPIFY THEME DEVELOPMENT
This repository contains an experimental theme for a Shopify storefront. It uses Liquid, CSS and minimal JavaScript to enhance features.

### Set Up
1. [Shopify Partner Account](https://shopify.dev.com) 
2. [Shopify Admin Rights](https://shopify.com)
3. [Shopify CLI](https://shopify.dev/docs/themes/tools/cli/install)
4. [Ruby](https://www.ruby-lang.org/en/documentation/installation/)
5. [Shopify Theme Check](https://github.com/Shopify/theme-check-vscode)

#### Shopify Partner Account
Headover to [Shopify Developers](https://shopify.dev.com) and create a developer account. Within the Shopify Partners homepage, click `Add Store -> Create Development Store`
Then follow the prompts provided in the Shopify UI to create your first Shopify Store Front.

#### Shopify Admin Rights
Note that we want to create our own custom Theme. However, to develop a theme, we have to check the progress of our development lifecycle. Therefore, 
a Shopify Account is required. Head over to [Shopify](https://shopify.com), login or (register if you do not have a Shopify Partner Account) and choose your
storefront from the list that appears. If successful, you will be redirected into the Shopify Admin account where you can easily customize your storefront theme.

In the admin page, click `Online Store -> Themes`. By default, Shopify provides a free customizable theme called Dawn based on the Shopify Liquid Language that 
is web native, HTML first and uses JavaScript if necessary to make the pages and apps performant and is a reference for building Shopify themes.

### Getting Started
1. Fork or clone [Shopify Dawn Theme](https://github.com/shopify/dawn) and customize it based on your personal requirements or build your own custom theme.
However, customizing Dawn is painless. 
2. Upload the local theme directory (forked Down or custom theme) to shopify and connect it to theme kit. To upload your custom theme, first, compress your local theme file, then headvoer to 
[Shopify](https://admin.shopify.com) -> `Online Store -> Themes -> Theme Library -> Add Theme -> Upload Zip file -> Publish`
3. Note down the theme Id 
- Within the admin dashboard, go to `Online Store -> Themes -> Theme Library -> Edit Code`
- Copy the trailing number from the url

4. Note down the API key from the theme kit access 
- Add `Theme Access` App within the Apps admin dashboard `Apps -> Search -> Theme Access`
- Within Theme Access, `Create password -> copy the emailed API Key`

### Local Theme Customization
I am assuming that you have cloned [Dawn](https://github.com/shopify/dawn) or you have your own custom theme that is [Shopify compliant](https://shopify.dev/themes/store/requirements)
In addition, ensure that you have installed Shopify CLI, Ruby and the Shopify Theme Check Extension.

1. Run `shopify theme check` on your bash terminal to run a shopify linter on the whole theme directory and follow the linting instructions to rectify errors, etc.
2. Run `theme configure -s {storefront name} -t {theme id} -p {Api Key}` on your bash terminal to generate a configuration file, `config.yml`
3. Run `theme watch --allow-live` on your bash terminal to sync your local theme directory development changes with your remote shopify storefront

