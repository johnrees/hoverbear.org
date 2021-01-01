These are the sources for my personal website.

To fork this, or test a change you may want to submit:

You'll need `cargo`. Get that by installing [Rustup](https://rustup.rs/). Next, install the [tagged Zola](https://github.com/getzola/zola/releases/tag/v0.12.2) via:

```bash
cargo install --git https://github.com/getzola/zola --ref 84ecd2ac5e2913426ea6e6a9dc55928e81d0df25
```

Run `zola serve` from a terminal in the site working directory. The first time you do this, it could take a long time, as it has to process a lot of images.

```bash
ana@autonoma:~/git/hoverbear/hoverbear.org$ zola serve
Building site...
-> Creating 86 pages (0 orphan), 14 sections, and processing 459 images
Done in 5.8s.

Web server is available at http://127.0.0.1:1111

Listening for changes in /home/ana/git/hoverbear/hoverbear.org{config.toml, content, sass, static, templates}
Press Ctrl+C to stop
```

You can interactively edit now. Changes should show up nearly immediately.

# Deployment

Seems the token described in https://help.github.com/en/articles/virtual-environments-for-github-actions#creating-and-using-secrets-encrypted-variables doesn't work for pyshing, so you'll need to add a CI secret called `TOKEN`. You'll also need to create a `gh-pages` branch and might need to change your default branch name from root.