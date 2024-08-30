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




