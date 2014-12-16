## Assignment Instructions 
### Time limit
The assigment should be solved and resent to Intelliplan within 3 days, starting when you recieve the assignment.

### Input / Output
The assigment will be tested with automatic acceptance tests. Therefore, pay special attention to formatting and reading. The input will be given on standard in, and output should be on standard out.
If there are any uncertaintes regarding the assignment, please don't hesitate to ask.
Just to be clear. The purpose of the assignment is for you to show how you code, reson and design. Not take forever and be difficult.

### Regarding tools and external libraries
You are not allowed to use any other external libraries than supplied. This is to make sure that everyone has the same starting point.

### Regarding the folder structure
Please resend the assigment intact. That is, in the same structure you got it, *with* all the files that came with it.

### Folder structure

#### Ruby
```bash
  developer_assignment
    |- bin/
        +- candidate_locator    # This should be a executable file. I.e. the main entry point for the assignment.
    |- lib/                     # This is where you put your code.
    |- specs/                   # This is where you put your tests.
    |- Gemfile                  # Gem dependencies
    |- Gemfile.lock             # Gems locked down
    |- LICENSE                  # License agreement
    |- rakefile                 # Helper tasks to build, test and distribute your code 
    |- README.md                # This document
```

#### HowTo's

##### Gems
The project uses [bundler](http://www.bundler.io) to manage gems.

All you need to do is to install bundler:
```bash
$ gem install bundler
```
And install the needed gems:

```bash
$ bundle install
```

##### Rake
There's currently only one rake task and that is spec.

```bash
$ bundle exec rake spec
```

#### Good Luck!

Kristoffer Roupé - Dec 2014, Stockholm Sweden.
