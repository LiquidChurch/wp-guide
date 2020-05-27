# Instructions
1. Install WP on web host.
    1. Download WPGraphQL from https://github.com/wp-graphql/, install, activate.
    1. Download WPGraphiQL from https://github.com/wp-graphql/wp-graphiql, install, activate.
    1. Run a test query in WPGraphiQL to ensure that WPGraphQL is working.
1. Install Node.js and npm.
1. Install Yarn.
1. Install Gatsby CLI: `yarn global add gatsby-cli`
1. Create a new Gatsby site using CLI: `gatsby new nameofsite gitrepo`
    1. Example: `gatsby new wpgatsby gatsbyjs/gatsby-starter-hello-world`
    1. Enter into the newly created directory: `cd wpgatsby`
    1. Install gatsby-source-graphql plugin: `yarn add gatsby-source-graphql`
    1. Install dotenv: `yarn add dotenv`
    1. Create .env.development and .env.production, they'll be used when running gatsby develop / build.
    1. Add .env.development to .gitignore.
1. Create/edit gatsby-config.js to utilize environment file:
```js
let activeEnv =
  process.env.GATSBY_ACTIVE_ENV || process.env.NODE_ENV || "development"

require("dotenv").config({
  path: `.env.${activeEnv}`,
})
```
1. Edit gatsby-config.js to enable gatsby-source-graphql.
```js
module.exports = ({
  plugins: [
    {
      resolve: 'gatsby-source-graphql',
      options: {
        typeName: `WPGraphQL`,
        fieldName: `wpgraphql`,
        url: `${wordPressUrl}/graphql`,
      },
    },
  ],
})
```
1. Remove index.js and page-2.js from the src/pages folder.
1. Create a page template file: /src/page/index.js
1. Create a post template file: /src/post/index.js
1. Create gatsby-node.js


## Notes
1. One doesn't have to use WPGraphQL to connect with Gatsby, there is also a gatsby-source-wordpress plugin which utilizes the REST API.
1. As of 0.8.1 WPGraphQL comes bundled with support for Posts, Pages, CPTs, Custom Taxonomies, Comments, Users, Menus, Plugins, Themes, and Settings.
1. One doesn't have to install the Gatsby CLI, one could use: `npx gatsby new nameofsite gitrepo` instead.
1. In our experience one frequently needs to blow away Gatsby installs. Doing this with npm is quite painful due to the number of packages in node_modules. Using Yarn provides local caching of the packages which significantly reduces the time to create a new Gatsby install.