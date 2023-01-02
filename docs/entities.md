## Working with Entities

### Lifecycle of an Entity

![image](https://user-images.githubusercontent.com/13553866/209671624-a8b630cf-2083-41a6-8cfd-eff244d2af39.png)

### Defining a Taxonomy for Your Entities

You can register different  _kinds_  of entities in Backstage and different  _types_  for each kind. By default, Backstage recognizes nine kinds, with pre-defined types in some cases. However, you can better define the kinds and types that represent your organization.

Let’s review the basic kinds that you’ll work with most of the time:

   -   [Component](https://backstage.io/docs/features/software-catalog/descriptor-format#kind-component)  refers to a software component bound to a repository and is deployable or linkable in an Artifactory. There are three known types of components: service, website, and library.
   -   [API](https://backstage.io/docs/features/software-catalog/descriptor-format#kind-api)  refers to an interface that can be exposed by a component. Backstage ships with support for OpenAPI, AsyncAPI, GraphQL, and gRPC, but it doesn’t have an opinion on the types you may use.
   -   [Resource](https://backstage.io/docs/features/software-catalog/descriptor-format#kind-resource)  refers to infrastructures like databases, storages, or CDNs. Bringing resources to your Catalog and associating them with components can be useful to visualize and optimize your system.
   -   [Group](https://backstage.io/docs/features/software-catalog/descriptor-format#kind-group)  is used to arrange users into teams or business units. Backstage lets you model your organization hierarchy using groups that belong to other groups.
   -   [User](https://backstage.io/docs/features/software-catalog/descriptor-format#kind-user)  refers to a person, such as an employee or contractor. Backstage requires you to assign all users to a group.
