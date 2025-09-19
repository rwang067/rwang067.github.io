
# Academic Pages

![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)

Academic Pages is a Github Pages template for academic websites.


# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running Locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.


# Maintenance 

Bug reports and feature requests to the template  should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.





## Add in 20250117

### Help

[https://jekylldo.cn/docs/installation/macos/]
[https://www.wenew.uk/2024/02/25/Mac-系统上安装-Jekyll/]
[https://www.jianshu.com/p/c70dc6d3af14]
[https://blog.csdn.net/haoaiqian/article/details/80194668]

### 0. 更改下载源
确认ruby版本不是3.1.3
ruby -v

更改下载源
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc
brew update

### 1. 安装 HomebrewPermalink
<!-- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" -->
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
(需按照提示手动选择安装源和国内配置源，尝试都选择1可以成功安装和配置，速度不慢)
source /Users/rui/.zprofile
( 安装成功 但还需要重启终端 或者 运行 source /Users/rui/.zprofile   否则国内地址无法生效)

### 2. 下载ruby
brew install ruby

<!-- // Error: No previously deleted formula found.
rm -rf /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core
brew update -->

添加ruby路径到环境变量
export PATH="/opt/homebrew/opt/ruby/bin:$PATH" （重启电脑后执行这步就可以）
<!-- echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc -->

which ruby 
(/opt/homebrew/opt/ruby/bin/ruby)
ruby -v
(终于显示ruby 3.4.1 (2024-12-25 revision 48d4efcb85) +PRISM [arm64-darwin23])

### 3. 在 mac 中安装 Jekyll 和依赖
// zsh: command not found: jekyll -->

sudo gem install --user-install bundler jekyll
(提示: WARNING:  You don't have /Users/rui/.gem/ruby/3.4.0/bin in your PATH)

export PATH="/Users/rui/.gem/ruby/3.4.0/bin:$PATH"
<!-- echo 'export PATH="/Users/rui/.gem/ruby/3.4.0/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc -->

sudo gem install --user-install bundler jekyll

### 4.通过bundle运行jekyll
jekyll -v

(/Users/rui/.gem/ruby/3.4.0/gems/bundler-2.6.3/lib/bundler/resolver.rb:355:in 'Bundler::Resolver#raise_not_found!': Could not find gem 'github-pages' in locally installed gems. (Bundler::GemNotFound))

bundle install

(/Users/rui/.gem/ruby/3.4.0/gems/bundler-2.6.3/lib/bundler/runtime.rb:319:in 'Bundler::Runtime#check_for_activated_spec!': You have already activated public_suffix 6.0.1, but your Gemfile requires public_suffix 5.1.1. Prepending `bundle exec` to your command may solve this. (Gem::LoadError))

bundle exec jekyll serve

访问 `localhost:4000` 


## Add in 20250522

### 1.  确定 ruby 版本

添加ruby路径到环境变量
export PATH="/opt/homebrew/opt/ruby/bin:$PATH" （重启电脑后执行这步就可以）
<!-- echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc -->

which ruby 
(/opt/homebrew/opt/ruby/bin/ruby)
ruby -v
(终于显示ruby 3.4.1 (2024-12-25 revision 48d4efcb85) +PRISM [arm64-darwin23])

### 2.  确定 Jekyll 和依赖

export PATH="/Users/rui/.gem/ruby/3.4.0/bin:$PATH" （重启电脑后执行这步就可以）

### 3.通过bundle运行jekyll
jekyll -v

/Users/rui/.gem/ruby/3.4.0/gems/bundler-2.6.3/lib/bundler/runtime.rb:319:in 'Bundler::Runtime#check_for_activated_spec!': You have already activated public_suffix 6.0.1, but your Gemfile requires public_suffix 5.1.1. Prepending `bundle exec` to your command may solve this. (Gem::LoadError)

bundle exec jekyll serve

访问 `localhost:4000` 

编辑页面

// 同步到 GitHub Page
git add .
git commit -m "add publications in 2025"
git push