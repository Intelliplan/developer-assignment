## Assignment Instructions 

The assignment description can be found at [iCALOC2014.md](iCALOC2014.md)

### Time limit
The assignment should be solved and resent to Intelliplan within 3 days, starting when you receive the assignment.

### Input / Output
The assignment will be tested with automatic acceptance tests. Therefore, pay special attention to formatting and reading. The input will be given on standard in, and output should be on standard out.
If there are any uncertainties regarding the assignment, please don't hesitate to ask.
Just to be clear. The purpose of the assignment is for you to show how you code, reason and design. Not take forever and be difficult.

### Regarding tools and external libraries
You are allowed to add in a testing and mocking framework of your choice. We won't however allow other "helping" frameworks. What comes with .net should be sufficient.

### Regarding the folder structure
Please resend the assigment intact. That is, in the same structure you got it, *with* all the files that came with it.

### Folder structure

#### C# .net
```bash
  developer_assignment
    |- src/
        +- bin/                 # Binary output
        +- obj/                 # Stuff you don't care about
        +- Properties/          # Assembly info
        +- icaloc2014.csproj    # Project cruft
        +- icaloc2014.sln       # Solution cruft
        +- Program.cs           # Main entry point of program
    |- Gemfile                  # Gem dependencies
    |- Gemfile.lock             # Gems locked down
    |- iCALOC2014.md            # The assignment
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

##### Nuget and packages
Nuget needs to be on you **PATH**.

To restore your packages simply run:

```bash
$ bundle exec rake restore
```


##### Rake

To compile the project
```bash
$ bundle exec rake quick_build
```

To run specs
```bash
$ bundle exec rake test
```


##### NOTE!
Please resend the assignment intact as a **zip-archive**. That is, in the same structure you got it, *with* all the files that came with it.

#### Good Luck!

Kristoffer Roupé - Dec 2014, Stockholm Sweden.
