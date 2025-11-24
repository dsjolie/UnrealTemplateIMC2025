# Unreal Engine Project

This repository contains an Unreal Engine project configured for version control with Git.

## Important Configuration Files

### .gitignore
The `.gitignore` file excludes temporary and generated files from version control, including:
- Intermediate build files
- Saved data
- Derived data cache
- Build output

**This is the most important file for keeping your repository clean.**

### Git LFS (Optional)
For small student projects, **Git LFS is usually not necessary**. Regular Git handles small binary files just fine.

However, if your project grows to include large assets (high-resolution textures, large models, videos), you can enable Git LFS:

1. Rename `.gitattributes.example` to `.gitattributes`
2. Follow the setup instructions below

## Setting Up Git LFS (If Needed)

### Installing Git LFS

**Windows:**
- Download the installer from [git-lfs.com](https://git-lfs.com)
- Run the installer and follow the prompts
- Or install via Git for Windows (includes LFS option during setup)

**macOS:**
```bash
brew install git-lfs
```

**Linux (Debian/Ubuntu):**
```bash
sudo apt-get install git-lfs
```

### Enabling LFS for This Project

1. Rename the example file:
   ```bash
   mv .gitattributes.example .gitattributes
   ```

2. Initialize Git LFS (one-time per machine):
   ```bash
   git lfs install
   ```

That's it! Future commits of large files will automatically use LFS. Existing files already committed will remain in regular Git (which is usually fine).

**Note about migrating existing files:** You can optionally migrate previously committed large files to LFS using `git lfs migrate import --everything --include="*.uasset,*.umap"`. This rewrites Git history to move old files into LFS storage. This is usually not necessary for student projects and can be disruptive if the repository is already shared.

## Working with the Project

After cloning, open `MyExercises.uproject` in Unreal Engine to start working on the project.
