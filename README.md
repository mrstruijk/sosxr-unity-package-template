# Packages in Unity

For more information on how to create packages and structure their directory formatting, see the resources below.
- [Unity Documentation](https://docs.unity3d.com/6000.1/Documentation/Manual/CustomPackages.html)
- [YouTube tutorial by 'git-amend'](https://www.youtube.com/watch?v=f2xW24xyDEg&t=190s)


----

# Regarding this template:

## Problem

Unity doesn't show `~` (tilde) folders, so you can't get there in the Editor.

## Solution

You need a local folder that is visible inside Unity, and not tracked by git.
You can do this by [symlinking](https://docs.unity.com/ugs/en-us/manual/devops/manual/symlink-support) from your `Samples~` folder to another folder without the `~` in the name. This template is setup to work with a folder called `InEditorSamples`, and below is how you simultaneously create and symlink to it. 

```bash
cd /ToFolder/OfPackage/

ln -s Samples~ InEditorSamples # Will create a symlinked folder called InEditorSamples
```

In a `.gitignore` track the folder and it's `.meta` so they don’t get added to the repo:

```bash 
InEditorSamples
InEditorSamples.meta
```

----


# README template:

# Repo Name

- By: 
- For: Leiden University SOSXR
- Fully open source: Feel free to add to, or modify, anything you see fit.


Simple overview of use/purpose.

## Description

An in-depth paragraph about your project and overview of use.

## Getting Started
### Installation

1. Open the Unity project you want to install this package in.
2. Open the Package Manager window.
3. Click on the `+` button and select `Add package from git URL...`.
4. Paste the URL of this repo into the text field and press `Add`. Make sure it ends with `.git`.

### Dependency
1. Minimum Unity version
2. Depends on [EnhancedLogger](https://github.com/solo-fsw/sosxr-unity-enhancedlogger)
3. 

### Executing program

* How to run the program
* Step-by-step bullets
```
code blocks for commands
```


## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```


## Authors

Contributors names and contact info


## Version History

* 0_0_2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0_0_1
    * Initial Release

See the CHANGELOG.md for more details.


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details


## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)

