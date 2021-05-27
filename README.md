# cyhoeddwn-guide

This is a repository for hosting the content in the wiki for the [cyhoeddwn](https://gitlab.com/merchygoedwig/cyhoeddwn) project. This project uses the [Jekyll](https://jekyllrb.com/) static site generator. Users with an installation of Ruby can host the site locally by running the following from a terminal:

```bash
# Optional (if you don't have bundler installed)
gem install bundler

cd cyhoeddwn-guide
bundle install
bundle exec jekyll serve --livereload
```

Alternatively, if you do not wish to maintain a local installation of Ruby, you may use the attached docker-compose file:

```bash
# You may need to prepend docker-compose with sudo depending on your install
docker-compose up -d
```

When you have set this up, navigate to [localhost:4000](http://localhost:4000)