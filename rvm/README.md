<pre><code>
<b>[~]$ rvm use 2.5.1@ToyRobotBook --create</b>
ruby-2.5.1 - #gemset created /Users/mikae/.rvm/gems/ruby-2.5.1@ToyRobotBook
ruby-2.5.1 - #generating ToyRobotBook wrappers..........
Using /Users/mikae/.rvm/gems/ruby-2.5.1 with gemset ToyRobotBook
<b>[~]$ gem list</b>

** LOCAL GEMS **

bigdecimal (default: 1.3.4)
bundler-unload (1.0.2)
cmath (default: 1.0.0)
csv (default: 1.0.0)
date (default: 1.0.0)
dbm (default: 1.0.0)
did_you_mean (1.2.0)
etc (default: 1.0.0)
executable-hooks (1.5.0)
fcntl (default: 1.0.0)
fiddle (default: 1.0.0)
fileutils (default: 1.0.2)
gdbm (default: 2.0.0)
gem-wrappers (1.3.2)
io-console (default: 0.4.6)
ipaddr (default: 1.2.0)
json (default: 2.1.0)
minitest (5.10.3)
net-telnet (0.1.1)
openssl (default: 2.1.0)
power_assert (1.1.1)
psych (default: 3.0.2)
rake (12.3.0)
rdoc (default: 6.0.1)
rubygems-bundler (1.4.5)
rvm (1.11.3.9)
scanf (default: 1.0.0)
sdbm (default: 1.0.0)
stringio (default: 0.0.1)
strscan (default: 1.0.0)
test-unit (3.2.7)
webrick (default: 1.4.2)
xmlrpc (0.3.0)
zlib (default: 1.0.0)
<b>[~]$ rvm gemset list</b>

gemsets for ruby-2.5.1 (found in /Users/mikae/.rvm/gems/ruby-2.5.1)
   (default)
=> ToyRobotBook
   global

<b>[~]$ which ruby</b>
/Users/mikae/.rvm/rubies/ruby-2.5.1/bin/ruby
<b>[~]$ which gem</b>
/Users/mikae/.rvm/rubies/ruby-2.5.1/bin/gem
<b>[~]$ rvm gemdir</b>
/Users/mikae/.rvm/gems/ruby-2.5.1@ToyRobotBook
<b>[~]$ which bundle</b>
/usr/local/bin/bundle
<b>[~]$ bundle version</b>
fatal: not a git repository (or any of the parent directories): .git
Bundler version 1.16.1 (2018-10-25 commit )
<b>[~]$ gem install bundler --no-ri --no-rdoc</b>
Fetching: bundler-1.17.0.gem (100%)
Successfully installed bundler-1.17.0
1 gem installed
<b>[~]$ which bundle</b>
/Users/mikae/.rvm/gems/ruby-2.5.1@ToyRobotBook/bin/bundle
<b>[~]$ bundle version</b>
Bundler version 1.17.0 (2018-10-25 commit 1fe7e93e9)
<b>[~]$ gem list</b>

** LOCAL GEMS **

bigdecimal (default: 1.3.4)
bundler (1.17.0)
bundler-unload (1.0.2)
cmath (default: 1.0.0)
csv (default: 1.0.0)
date (default: 1.0.0)
dbm (default: 1.0.0)
did_you_mean (1.2.0)
etc (default: 1.0.0)
executable-hooks (1.5.0)
fcntl (default: 1.0.0)
fiddle (default: 1.0.0)
fileutils (default: 1.0.2)
gdbm (default: 2.0.0)
gem-wrappers (1.3.2)
io-console (default: 0.4.6)
ipaddr (default: 1.2.0)
json (default: 2.1.0)
minitest (5.10.3)
net-telnet (0.1.1)
openssl (default: 2.1.0)
power_assert (1.1.1)
psych (default: 3.0.2)
rake (12.3.0)
rdoc (default: 6.0.1)
rubygems-bundler (1.4.5)
rvm (1.11.3.9)
scanf (default: 1.0.0)
sdbm (default: 1.0.0)
stringio (default: 0.0.1)
strscan (default: 1.0.0)
test-unit (3.2.7)
webrick (default: 1.4.2)
xmlrpc (0.3.0)
zlib (default: 1.0.0)
<b>[~]$ bundle gem toy_robot</b>
Creating gem 'toy_robot'...
Do you want to license your code permissively under the MIT license?
This means that any other developer or company will be legally allowed to use your code for free as long as they admit you created it. You can read more about the MIT license at https://choosealicense.com/licenses/mit. y/(n): y
MIT License enabled in config
      create  toy_robot/Gemfile
      create  toy_robot/lib/toy_robot.rb
      create  toy_robot/lib/toy_robot/version.rb
      create  toy_robot/toy_robot.gemspec
      create  toy_robot/Rakefile
      create  toy_robot/README.md
      create  toy_robot/bin/console
      create  toy_robot/bin/setup
      create  toy_robot/.gitignore
      create  toy_robot/.travis.yml
      create  toy_robot/.rspec
      create  toy_robot/spec/spec_helper.rb
      create  toy_robot/spec/toy_robot_spec.rb
      create  toy_robot/LICENSE.txt
Initializing git repo in /Users/mikae/toy_robot
Gem 'toy_robot' was successfully created. For more information on making a RubyGem visit https://bundler.io/guides/creating_gem.html
<b>[~]$ mv toy_robot book_toy_robot</b>
<b>[~]$ cd book_toy_robot/</b>
<b>[book_toy_robot]$ git status</b>
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   .gitignore
        new file:   .rspec
        new file:   .travis.yml
        new file:   Gemfile
        new file:   LICENSE.txt
        new file:   README.md
        new file:   Rakefile
        new file:   bin/console
        new file:   bin/setup
        new file:   lib/toy_robot.rb
        new file:   lib/toy_robot/version.rb
        new file:   spec/spec_helper.rb
        new file:   spec/toy_robot_spec.rb
        new file:   toy_robot.gemspec

<b>[book_toy_robot]$ git add .</b>
<b>[book_toy_robot]$ git commit -m "'$ bundle gem toy_robot' Creates a skeleton for creating a rubygem"</b>
[master (root-commit) c9c7a68] '$ bundle gem toy_robot' Creates a skeleton for creating a rubygem
 14 files changed, 189 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 .rspec
 create mode 100644 .travis.yml
 create mode 100644 Gemfile
 create mode 100644 LICENSE.txt
 create mode 100644 README.md
 create mode 100644 Rakefile
 create mode 100755 bin/console
 create mode 100755 bin/setup
 create mode 100644 lib/toy_robot.rb
 create mode 100644 lib/toy_robot/version.rb
 create mode 100644 spec/spec_helper.rb
 create mode 100644 spec/toy_robot_spec.rb
 create mode 100644 toy_robot.gemspec
<b>[book_toy_robot]$ git remote add origin git@github.com:baxter2/book_toy_robot.git</b>
<b>[book_toy_robot]$ git push -u origin master</b>
Counting objects: 20, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (18/18), done.
Writing objects: 100% (20/20), 4.35 KiB | 891.00 KiB/s, done.
Total 20 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/baxter2/book_toy_robot/pull/new/master
remote:
To github.com:baxter2/book_toy_robot.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
</pre></code>
