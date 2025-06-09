# berrylium-blog

This repository contains the source code and configuration files for [my Hexo blog](https://berrylium0078.github.io).

## Cloning a starter

Before getting started, ensure that you have `git` and `npm` installed.

```sh
git clone --depth=1 --branch starter https://github.com/berrylium0078/berrylium-blog my-cloned-blog
cd my-cloned-blog
npm install
```

## Customization

To customize the blog, edit the *_config.redefine.yml* and *_config.yml* files.

Custom fonts are enabled by default:
- *Noto Sans CJK SC* for Chinese text
- *Noto Sans* for English text
- *Fira Code* for code blocks

This blog uses the *Redefine theme*. For detailed configuration options, refer to the [official documentation](https://redefine-docs.ohevan.com).

In addition, several markdown-it plugins are integrated via hexo-renderer-markdown-it-plus. For more information, refer to the *_config.yml* file and the documentation for each plugin.
