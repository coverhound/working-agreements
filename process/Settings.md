[Main](../README.md) >
[Process](./README.md)

# Settings

## Configuration Files and the Settings Repo

Sensitive information (such as API keys and passwords) and configuration data
are kept in yaml files that are loaded into our applications upon
initialization. Configuration settings for all applications are centralized in
the [Settings Repo](https://github.com/coverhound/settings-files).

## Adding / Updating Settings

1. Add the settings to the pertinent development config file:
   `[project-name]/development/[settings-file-name].yml`
2. Create a pull request to the [Settings
   Repo](https://github.com/coverhound/settings-files)
3. Ask your tech lead to add the settings to the staging config file:
   `[project-name]/staging/[settings-file-name].yml`
4. Create a ticket in the Pivotal devops project to update the production
   settings
5. Once the PRs to the settings repo have been merged and the devops ticket has
   been completed, code that depends on the new settings can be safely released.

## Local Settings

Settings can be configured for a specific environment by adding the file
`/config/settings_local.yml`. This file will be merged with `settings.yml` upon
initialization of the app, with keys in `settings_local` winning the merge. This
is useful for local development, or for configuring a specific staging
environment.
