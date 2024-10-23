## Encyclopedia

To see the main page of this notebook, please go to: [index.md](index.md), or visit the website linked.

The section below is for my own reference:


### To setup

1. Clone the repo. (This assumes Git was installed)
2. Easier to follow Jekyll installation: https://jekyllrb.com/docs/installation/
3. If for some reason, the Gemfile does not exist, do `bundle init` then `bundle add GEM_NAME` where `GEM_NAME` is replaced with the name(s) of the necessary Gems (Ruby packages). At the time of this writing, this repo would need `jekyll`, `jekyll-feed` and `webrick`. 
4. Otherwise if the Gemfile already existed, do `bundle install`. As of July 2024, the Gemfile is tracked by the git repo, and step 3 will likely will never be needed again.

### To test locally

Run: `bundle exec jekyll serve`

### To update website

Run: `git push origin master`

This only pushes to GitHub what is currently in the `master` branch, so be sure to commit any wanted changes to the branch.

### Other things

TBD.