## EXPERIMENTAL SHOPIFY THEME DEVELOPMENT
This repository contains an experimental theme for a Shopify storefront. It uses Liquid, CSS and minimal JavaScript to enhance features.

### Set Up
1. [Shopify Partner Account](https://shopify.dev.com) 
2. [Shopify Admin Rights](https://shopify.com)
3. [Shopify CLI](https://shopify.dev/docs/themes/tools/cli/install)
4. [Ruby](https://www.ruby-lang.org/en/documentation/installation/)
5. [Shopify Theme Check](https://github.com/Shopify/theme-check-vscode)

#### Shopify Partner Account
Head over to [Shopify Developers](https://shopify.dev.com) and create a developer account. Within the Shopify Partners homepage, click `Add Store -> Create Development Store`. Then follow the prompts provided in the Shopify UI to create your first Shopify Store Front.

#### Shopify Admin Rights
Note that we want to create our own custom theme which requires constant monitoring of the UI during the development lifecycle. Therefore, 
a Shopify Account is required and a link between the remote Shopify storefront and the local custom theme is necessary. 

Head over to [Shopify](https://shopify.com), login or (register if you do not have a Shopify Partner Account) and choose your
storefront from the list that appears. If successful, you will be redirected into the Shopify Admin account where you can easily customize your storefront theme.

In the admin page, click `Online Store -> Themes`. By default, Shopify provides a free customizable theme called [Dawn](https://github.com/shopify/dawn) based on the Shopify Liquid Language. Dawn is web native, HTML first and uses JavaScript only when necessary. This ensures that web apps are performant. Furthermore, Dawn is a reference for building Shopify themes.

### Getting Started
1. Fork or clone [Shopify Dawn Theme](https://github.com/shopify/dawn) and customize it based on your personal requirements or fork and clone this repository.
- `$ git clone git@github.com:{your-github-username}/shopify-temp-theme.git`
- `$ cd shopify-temp-theme` or `$ cd dawn`
- `$ shopify theme check`

2. Upload the local theme directory (forked Dawn or custom theme) to shopify and connect it to theme kit. To upload your custom theme;
-  First, compress your local theme file
-  Headvoer to [Shopify](https://admin.shopify.com) -> `Online Store -> Themes -> Theme Library -> Add Theme -> Upload Zip file -> Publish`

3. Note down the theme Id 
- Within the admin dashboard, go to `Online Store -> Themes -> Theme Library -> Edit Code`
- Copy the trailing number from the url

4. Note down the API key from the theme kit access 
- Add `Theme Access` App within the Apps admin dashboard `Apps -> Search -> Theme Access`
- Within Theme Access, `Create password -> copy the emailed API Key`

5. Generate a yaml configuration file
- Run `$ theme configure -s {storefront name} -t {theme id} -p {Api Key}` on your bash terminal

6. Sync local file to remote stoirefront for local changes
- Run `$ theme watch --allow-live` on your bash terminal

### Contributing Code
You can follow these steps to contribute code or create issues in this repository.

>:information_source: I'll assume you're already set up with Git and GitHub (if you're not familiar with these, [start with these docs](https://docs.github.com/github/getting-started-with-github/quickstart/set-up-git)).

1. Fork and clone this repository then create a new branch
- `$ git clone git@github.com:{your-github-username}/shopify-temp-theme.git`
- `$ git branch {new branch name}`

2. Checkout to the new branch
- `$ git checkout -b {new branch name}`

3. Launch a development server
- `$ shopify theme dev`

4. Add your changes to the codebase
5. Commit your changes
- `$ git commit -a -m "Change #: your commit message"`

6. Push commit to your forked repository
- `$ git push origin {new branch name}`

7. Open a [pull request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) in this repository
8. Merge your pull request

### Copyright & Licence Info
MIT Copyright (c) 2023 Wayne Kirimi

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
