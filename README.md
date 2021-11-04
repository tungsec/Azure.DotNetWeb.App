# App Build Pipeline
* A repository for application source code.
* Every git-push to the main branch of the repository initiates a pipeline run.
* The build pipeline builds adn publishes the app Docker image and tests it. If everything has succeeded, it updates the release id variable in the Azure DevOps Pipeline Library (variable groups).
* The release pipeline is triggered by succesfully finishing the Release stage of the build pipeline.
```
.
├── Dockerfile
├── DotNetWebApp.csproj
├── Pages
│   ├── Error.cshtml
│   ├── Error.cshtml.cs
│   ├── Index.cshtml
│   ├── Index.cshtml.cs
│   ├── Privacy.cshtml
│   ├── Privacy.cshtml.cs
│   ├── Shared
│   │   ├── _Layout.cshtml
│   │   └── _ValidationScriptsPartial.cshtml
│   ├── _ViewImports.cshtml
│   └── _ViewStart.cshtml
├── Program.cs
├── Properties
│   └── launchSettings.json
├── README.md
├── Startup.cs
├── appsettings.Development.json
├── appsettings.json
├── azure-pipelines.yml
└── wwwroot
    ├── css
    │   └── site.css
    ├── favicon.ico
    ├── js
    │   └── site.js
    └── lib
        ├── bootstrap
        ├── jquery
        ├── jquery-validation
        └── jquery-validation-unobtrusive
```