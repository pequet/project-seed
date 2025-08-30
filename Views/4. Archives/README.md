# Seed Project: Public/Private Repository Structure

This directory contains the standard boilerplate for a project's `Public Repositories` view. It provides a starting point for managing both a public-facing GitHub repository and its associated private assets.

## Structure

-   **/cursor-project-boilerplate/**
    This folder is a placeholder for your public-facing GitHub repository. All files that will be committed to the public submodule belong here. **You must rename this folder to match your actual repository name.**

-   **/private/**
    This folder is for private assets that you want to track within the parent framework but *not* in the public project repository. This can include sensitive notes, development logs, or configuration files (`.cursor`, `.specstory`, `memory-bank`, etc.).

## Usage

When you create a new project by copying the `Seed` directory:

1.  Navigate to `Views/Public Repositories/`.
2.  Rename `cursor-project-boilerplate` to your actual GitHub repository name (e.g., `my-awesome-project`).
3.  Initialize the renamed folder as a public Git repository.
4.  Use symlinks to connect the public repo to any necessary assets in the `private` folder. 

## Framework Context for the Developer

> [!NOTE]
> The following section explains how this directory fits within the larger framework. This context is crucial for development within the framework but can be disregarded by external users viewing a standalone public repository.

This `Public Repositories` directory does not exist in a vacuum. It is a `View` within the master `Projects/Seed` project. The `Seed` project itself is a complete, self-contained TRI entity with the standard MVC structure:

-   **/Models/**: Contains the project's data, knowledge, and state, including:
    -   `Models/0. Inbox/`: The capture point for all new ideas, notes, and raw information related to the project.
    -   `Models/4. Archives/`: The destination for files that are no longer active but must be preserved, following the framework's "never delete" principle.
-   **/Views/**: Contains the presentational components, including this `Public Repositories` directory.
-   **/Controllers/**: Contains the logic and methods for the project.

When you work on a project created from this seed, you are expected to use the full methodology. Ideas go into the `Inbox`, and files are moved to `Archives` instead of being deleted. This structure provides the necessary context and tooling for robust, long-term development within the ecosystem.

## Support the Project

If you find this project useful and would like to show your appreciation, you can:

- [Buy Me a Coffee](https://buymeacoffee.com/pequet)
- [Sponsor on GitHub](https://github.com/sponsors/pequet)

Your support helps in maintaining and improving this project. 

## License

This project is licensed under the MIT License.