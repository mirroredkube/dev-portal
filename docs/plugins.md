## Plugins

Plugins define, to a large extent, what your Backstage instance can do. There are plugins that give you extra features and plugins that bring third-party information into your instance. Installing plugins will require you to add their packages to your dependencies.

- Your Backstage app is a single-page application whose features you define with plugins.
- Backstage plugins are implemented as React frontends that you can plug into a Backstage app. 
- The plugin system in Backstage is built around extensibility and composability.

Backstage plugins may also offer a backend counterpart that implements the API that the plugin frontend consumes. In some cases, teams opt out of a plugin’s frontend and only consume the plugin’s backend. This means they have to build and maintain their own frontend plugin but gain the ability to control exactly how they want their UI to work. 

#### Categories of Plugins

There are a few dozen plugins available in Backstage at the moment, with very different features and objectives. I’m proposing a loose categorization of plugins to make it easier to talk about plugins.

-   **Feature plugins:**  provides functionality to Backstage, such as the core plugins Catalog, Scaffolder, and TechDocs, and other plugins such as Org, Badges, and Tech Insights.
-   **Extension plugins:**  extend a feature plugin with added functionality, for example, the gRPC module for API Docs or the Google Analytics module for the Analytics plugin.
-   **Integration plugin:**  brings information from a vendor or external service into Backstage, typically in the form of a widget in the entity page or a standalone page. For example, the Argo CD plugin, GitHub Pull Request Board, or the CircleCI plugin.
-   **Entity providers:**  bring entities into Backstage from their respective sources, for example, the Azure Entity Provider and the LDAP integration.

By no means is this an official typology, nor will you find these categories in the plugins at all.

#### Installing Plugins

Depending on the category of the plugin you want to install, you’ll need to do certain steps in different places.

To install a plugin, you’ll need to add their packages to your instance, and depending on the plugin, you might have to add annotations to your metadata files, authorize your instance to access a third-party service, or add the plugin’s UI into your instance.

In general, you’ll need to add the plugin package to your instance. Plugins may implement the backend, the frontend, and shared logic as separate packages. Although it might seem bloated in the beginning, this separation of concerns allows you to install only what you need and provides more flexibility to the ecosystem. If you were to use the plugin’s provided UI, you’ll have to install all the packages. But if you want to provide your own UI, you can only use the plugin’s backend.  

Other than adding the plugin’s packages into your instance, feature plugins usually require you to set up information in the entities’ YAML files. For example, adding documentation annotations for TechDocs in each YAML file. 

In the case of integration plugins, after you have added their packages to your instance, you’ll need to authorize Backstage to access the third-party service. The most common way to do this is via an authorization token for your instance to access the third-party API. 

Finally, most plugins will require you to add their UI into your instance’s frontend using React. For example, adding a link in a navigation menu, or a widget on the entity page. Some plugins allow you to customize these widgets by passing props into them. 
