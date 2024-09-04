# 🍥fuwa-fuwari (fuwari customized by h-nakashima)

A static blog template built with [Astro](https://astro.build). Customized version by h-nakashima.

[**🖥️ Live Demo (Cloudflare Pages)**](https://fuwari-template.pages.dev)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;
[**📦Original Version**](https://github.com/saicaca/fuwari)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;
[**🌏 中文**](https://github.com/saicaca/fuwari/blob/main/README.zh-CN.md)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;
[**🌏 日本語**](https://github.com/saicaca/fuwari/blob/main/README.ja-JP.md)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;
[**🌏 한국어**](https://github.com/saicaca/fuwari/blob/main/README.ko.md)

> README version: `2024-09-01`

![Preview Image](./sample_home.png)

## ✨ Features
### Original Repository
- [x] Built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com)
- [x] Smooth animations and page transitions
- [x] Light / dark mode
- [x] Customizable theme colors & banner
- [x] Responsive design
- [ ] Comments
- [x] Search
- [ ] TOC

### Additional Features in This Repository
- [x] Moved sidebar to the right
- [x] Added recent posts widget to sidebar
- [x] Google Analytics support
- [ ] Page view counter
- [ ] Added access ranking to sidebar
- [ ] Google Adsense support

## 🚀 How to Use

1. [Generate a new repository](https://github.com/saicaca/fuwari/generate) from this template or fork this repository.
2. To edit your blog locally, clone your repository, run `pnpm install` AND `pnpm add sharp` to install dependencies.
   - Install [pnpm](https://pnpm.io) `npm install -g pnpm` if you haven't.
3. Edit the config file `src/config.ts` to customize your blog.
4. Run `pnpm new-post <filename>` to create a new post and edit it in `src/content/posts/`.
5. Deploy your blog to Vercel, Netlify, GitHub Pages, etc. following [the guides](https://docs.astro.build/en/guides/deploy/). You need to edit the site configuration in `astro.config.mjs` before deployment.

### How to Apply Template Updates to a Cloned Repository
#### For the First Update
This section describes how to incorporate updates from the [template](https://github.com/h-nakashima/fuwa-fuwari/generate) into a cloned repository and create a PR using the `feature/template-sync` branch.

1. **Create a New Branch**
   Create a `feature/template-sync` branch within the cloned repository to apply the template changes.
   ```bash
   git checkout -b feature/template-sync
   ```

2. **Add the Template Repository as a Remote**
   Add the template repository `git@github.com:h-nakashima/fuwa-fuwari.git` as a remote.
   ```bash
   git remote add template git@github.com:h-nakashima/fuwa-fuwari.git
   ```

3. **Fetch Changes from the Template Repository**
   Fetch the latest changes from the template repository.
   ```bash
   git fetch template
   ```

4. **Merge Template Changes into the Cloned Repository**
   Merge the latest changes from the `main` branch of the template repository into the `feature/template-sync` branch.
   ```bash
   git merge template/main --allow-unrelated-histories
   ```

   If conflicts occur, resolve them manually and complete the merge.

5. **Commit the Changes**
   After resolving any conflicts, review the changes as needed, and commit them.
   ```bash
   git commit -m "Merged updates from template repository"
   ```

6. **Push the Branch to Remote**
   Push the `feature/template-sync` branch to the remote repository.
   ```bash
   git push origin feature/template-sync
   ```

7. **Create a Pull Request on GitHub**
   On GitHub, create a pull request from the `feature/template-sync` branch in the cloned repository. Fill in the PR title and description appropriately to ensure the template repository's changes are reflected in the cloned repository.

#### For Subsequent Updates

1. **Switch to the Branch**
   Switch to the `feature/template-sync` branch to apply the template changes.
   ```bash
   git checkout feature/template-sync
   ```

2. **Fetch Changes from the Template Repository**
   Fetch the latest changes from the template repository.
   ```bash
   git fetch template
   ```

3. **Merge Template Changes into the Cloned Repository**
   Merge the latest changes from the `main` branch of the template repository into the `feature/template-sync` branch.
   ```bash
   git merge template/main
   ```

   If conflicts occur, resolve them manually and complete the merge.

4. **Commit the Changes**
   After resolving any conflicts, review the changes as needed, and commit them.
   ```bash
   git commit -m "Merged updates from template repository"
   ```

5. **Push the Branch to Remote**
   Push the `feature/template-sync` branch to the remote repository.
   ```bash
   git push
   ```

6. **Create a Pull Request on GitHub**
   On GitHub, create a pull request from the `feature/template-sync` branch in the cloned repository. Fill in the PR title and description appropriately to ensure the template repository's changes are reflected in the cloned repository.

## ⚙️ Frontmatter of Posts

```yaml
---
title: My First Blog Post
published: 2023-09-09
description: This is the first post of my new Astro blog.
image: /images/cover.jpg
tags: [Foo, Bar]
category: Front-end
draft: false
---
```

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                             | Action                                           |
|:------------------------------------|:-------------------------------------------------|
| `pnpm install` AND `pnpm add sharp` | Installs dependencies                            |
| `pnpm clean`                        | Delete build output and cache                    |
| `pnpm dev`                          | Starts local dev server at `localhost:4321`      |
| `pnpm build`                        | Build your production site to `./dist/`          |
| `pnpm preview`                      | Preview your build locally, before deploying     |
| `pnpm new-post <filename>`          | Create a new post                                |
| `pnpm astro ...`                    | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro --help`                 | Get help using the Astro CLI                     |
