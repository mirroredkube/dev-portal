## TechDocs

TechDocs let you bring documentation for software components into your Backstage instance. TechDocs can generate your documentation on the fly, but it is better to delegate generation to the CI system. All the documentation is written in standard markdown syntax.

TechDocs is based on markdown files stored alongside the code that they document to make it easier for developers to keep it up to date.

Docs are associated with a component when their YAML file includes the backstage.io/techdocs-ref annotation. The annotation tells Backstage that there are docs available that it should show to the user.

TechDocs goes through three stages to make documentation from markdown files in a repo to pages deployed in your Backstage instance: 
- preparation 
- generation
- publishing

You can tell TechDocs that you will opt out of its built-in generation—by specifying techdocs.builder to external in the TechDocs annotation—and publish the generated assets in a Cloud storage. Typically, you’d rely on your CI system to generate documentation when a Pull Request is merged. The generated assets will then be published in a Cloud storage, such as an S3 Bucket, and your Backstage instance would read them when needed. 

#### Writing TechDocs

TechDocs generates the documentation using  [MkDocs](https://www.mkdocs.org/)  and styles it using  [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), so there is nothing particularly “Backstage” about how you write your markdown files or configurations.

You can  [configure the navigation](https://www.mkdocs.org/user-guide/writing-your-docs/#configure-pages-and-navigation)  in the  `**mkdocs.yml**`  for your documentation, as you would normally do with MkDocs.

For writing the documentation, you can use standard markdown. The Python library in charge of the generation complies with standard  [markdown syntax](https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown), with very minor differences.

For linking files within your docs, you can use  [standard relative markdown links](https://www.mkdocs.org/user-guide/writing-your-docs/#linking-to-pages).

