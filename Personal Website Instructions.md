### Personal Website Instructions

Recall Command + Shift + . is required to show hidden files on Mac!

1. Install separate version of Ruby that doesn't interfere with the one provided by Apple
   1. Make sure you have Homebrew installed
   2. In terminal, call `brew install chruby ruby-install`
   3. Then call `ruby-install ruby`
   4. Call `brew info chruby` to find out installed directory
   5. Add what it says to the `.zshrc`. It should be something like `source /opt/homebrew/opt/chruby/share/chruby/chruby.sh`
   6. To enable auto-switching, add `source /opt/homebrew/opt/chruby/share/chruby/auto.sh`
   7. Lastly, update the `PATH` directory in `.zshrc` by adding the following line: `export PATH="/Users/keshavakatti/.rubies/ruby-3.3.4/bin:$PATH"`
   8. Quit and restart terminal
   9. Check which version of Ruby is being using by calling `which ruby`. It should *not* be `/usr/bin/ruby`. Then call `ruby -v`. It should be 3.1.3 or later. In this case, it is 3.3.4
2. Install bundler by calling `gem install bundler jekyll`
3. Clone GitHub repository at https://github.com/Siming-He/siming-he.github.io 
4. `cd` into root directory where `_config.yml` is located. In this case, it is `/Users/keshavakatti/Documents/GitHub/personal-website`
5. Run `bundle install` (may also need `bundle update`)
6. If using Ruby version 3.0.0 (which we are), the next step may fail. This can be fixed by adding `webrick` to our dependencies by calling `bundle add webrick`
7. Run `bundle exec jekyll serve`
8. Browse to http://localhost:4000/hydejack-starter-kit/