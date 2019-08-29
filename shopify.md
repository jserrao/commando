## Shopify Themekit - for modifying existing Shopify Themes
01.   `brew tap shopify/shopify` (sets up shopify stuff in the Homebrew brain)
02.   `brew install themekit` (puts themekit in there)
03.   `theme get --list -p=[your-password] -s=[you-store.myshopify.com]` (helps you to see what Shopify sees for your themes, retrieves the theme ID)
04.   `theme get -p=[your-password] -s=[you-store.myshopify.com] -t=[your-theme-id]` (retrieves existing shopify theme into whatever directory you're currently in on the CLI)
05.   `theme new --password=[your-password] --store=[your-store.myshopify.com] --name=[theme name]` (makes a completely new theme, but honestly if you're doing that, you should probably be using [Slate](https://shopify.github.io/slate/docs/about)
06.   `theme deploy` (pushes the theme you're working on up to Shopify and OVERWRITES whatever is on Shopify - please use version control locally!)
07.   `theme watch` (actively watches your theme files and pushes them up to Shopify and OVERWRITES whatever is on Shopify!)