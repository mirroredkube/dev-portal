### List of Adoptors:

[backstage/ADOPTERS.md at master · backstage/backstage (github.com)](https://github.com/backstage/backstage/blob/master/ADOPTERS.md)

Executive buy-in is crucial for their adoption

### Technlogy stack:

Backstage is an aggregator. But it connects popular technologies

1.  YAML - primary source of metadata
2.  React - App UI for plugins
3.  Node - for custom plugins and processors
4.  TypeScript - App
5.  Docker - to build locally, TechDocs / services
6.  Monorepos - Backstage is built as a monorepo
7.  Symantic Versioning - Minor version every month

#### Self hosted backstage:

-   Most popular: Kubernetes / AKS

##### Advantages:
-   No limit to customization

##### Disadvantages:
-   Considerable learning curve for backstage internals
-   Operations: Upgrade & patching monthly
-   Plugin upgrades - separate
-   Dedicated engineer / team for BAU
-   Need for a separate scrum team

#### Managed Backstage:
-   Roadie.io

#####   Advantages:

-   SaaS Production instance
-   No knowledge of Node and React required
-   All plugin setup is through UI / Wizard
-   Updates happen automatically
-   Fewer people in BAU / lighter skills
-   SLAs available

##### Disadvantages:

-   Less flexible for customization
