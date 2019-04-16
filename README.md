# PySCF website 

The PySCF website runs on GitHub Pages using Jekyll, with styling based
on Twitter Bootstrap.  GitHub Pages runs Jekyll automatically and builds
the website out of source files contained in this repository.

## Bootstrap

The site uses a few drop-in files from a Bootstrap distribution, which require
special placement for Jekyll/GitHub Pages compatibility.  Sass files that
compile to CSS are found in `_sass/bootstrap/*` and Javascript files are found in
`assets/javascript/bootstrap/*`.  These files need to be replaced by hand in
order to use a new Bootstrap distribution.

## Local development and testing

The Jekyll-based build requires a [Ruby]() installation. Next, install Bundler
```bash
$ gem install bundler
```

In the top level directory of the website repository, install Jekyll and other
dependencies from the GitHub Pages gem (see `Gemfile`):
```
bundle install
```

To keep the site up to date with the GitHub Pages gem,
```bash
$ bundle update
```

After making any changes, you can build and view the site locally,
```bash
bundle exec jekyll serve
```
which will build and serve the website out of `http://127.0.0.1:4000`.

## References

- [Official Jekyll page on GitHub Pages](https://jekyllrb.com/docs/github-pages/)
- [Setting up your GitHub Pages site locally with
Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
- [Creating and Hosting a Personal Site on
  GitHub](http://jmcglone.com/guides/github-pages/)
- [5 Steps To Add Bootstrap 4 To Jekyll The Right
Way](https://simpleit.rocks/ruby/jekyll/tutorials/how-to-add-bootstrap-4-to-jekyll-the-right-way/)
- [Bootstrap 4 Github
Pages](https://nicolas-van.github.io/bootstrap-4-github-pages/)

