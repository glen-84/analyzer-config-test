# AnalyzerConfigTest

Shareable [analyzer configuration](https://learn.microsoft.com/en-us/visualstudio/code-quality/use-roslyn-analyzers) for C# applications.

## Installation

- Set the following environment variables:
    - `GITHUB_USERNAME` – your GitHub username.
    - `GITHUB_NUGET_TOKEN` – the value of a [personal access token](https://github.com/settings/tokens) (scopes: `read:packages`).
- Add a `nuget.config` file with the following contents:
    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <packageSources>
            <add key="github" value="https://nuget.pkg.github.com/glen-84/index.json" />
        </packageSources>

        <packageSourceCredentials>
            <github>
                <add key="Username" value="%GITHUB_USERNAME%" />
                <add key="ClearTextPassword" value="%GITHUB_NUGET_TOKEN%" />
            </github>
        </packageSourceCredentials>
    </configuration>
    ```
- Run `dotnet add package Glen84.AnalyzerConfigTest.Applications`.
