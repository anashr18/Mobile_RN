# Mobile_RN

This repository contains React-Native app developments and experiments.

## Resolving Git Issues on macOS with External Hard Drive as Workspace

When using an external hard drive as a workspace on macOS, you might encounter issues with files prefixed with '._'. These are AppleDouble files created by macOS to store extended attributes and can cause problems with Git.

### Steps to Resolve

1. **Find and Remove AppleDouble Files:**
   Use the following command to locate and delete all files with the '._' prefix:

   ```sh
   find . -name '._*' -exec rm -f {} \;
   ```

2. **Repack the Git Repository:**
   After removing the AppleDouble files, repack the repository to optimize it:

   ```sh
   git repack -a -d --depth=250 --window=250
   ```

Following these steps will help you maintain a clean and efficient Git repository when working with an external hard drive on macOS.

## Create a new expo app

```sh
npx create-expo-app@latest --template blank RNProject
```

## Resolving "Too many files open" issue with Expo on macOS

If you encounter the "Too many files open" error while using Expo on macOS, you can resolve it by installing Watchman. Watchman helps to watch file changes and can handle a large number of files efficiently.

1. **Install Watchman:**
   Use Homebrew to install Watchman:

   ```sh
   brew install watchman
   ```

2. **Rebuild the Project:**
   After installing Watchman, delete the `node_modules` directory and reinstall the dependencies. Then, start the project again

   ```sh
   rm -rf node_modules
   npm install
   npm start
   ```
