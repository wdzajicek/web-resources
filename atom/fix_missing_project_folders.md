# Fix Missing Project Files & Folders

When installing atom for the first time, it decides to ignore all paths that appear in your `.gitignore` file. This is completely impractical for our development.

Actually, I have never found a practical application where I needed this setting—and it seems like a silly default for developers/programers, etc.. Of all the people who need to see the hidden files of a project, I would think programers/developers/etc.—the main users of this kind of text-editor—would always want to keep tabs on _everything_ in the project.

If you leave it set to the atom default, you won't be able to see the `_site/` folder containing the project's build—that's helpful, right?

## The Fix

The problem resides in a setting for the "tree-view" core-package of atom. All you have to do is disable the `Hide VSC Ignored Files` setting.

1. Go to atom's main settings screen (Cmd + ,).
2. Go to the `Packages` settings.
3. Type `tree-view` in the `Filter packages by name` field: You should get a single result in `Core Packages`
4. Open tree-view's settings.
5. Find and disable the `Filter packages by name` by clearing the checkmark
6. Done.

![Screenshot of the Hide VSC Ignored Files](/atom/assets/img/hide-folders-setting.png)
