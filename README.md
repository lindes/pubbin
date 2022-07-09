lindes's pubbin
===============

Public 'bin' directory, for commands I think others would find useful.

I'll gradually migrate things from my personal private `$HOME/bin`
into this repository.  You're encouraged to check it out as
`$HOME/lindes-bin` or similar, and then puth that into your `$PATH`,
if you think you'll find these tools generally useful.  Or pick and
choose as you see fit.

Pull requests, bug reports, and more are welcome, using
[github](https://github.com/lindes/pubbin).

## How to use these tools:

Basically, you want to clone this REPO somewhere where it can be found
in your shell's PATH.  (Or, clone it and copy individual files somewhere
that is.)

One simple way to do this might be to run the following commands:

```shell
git clone https://github.com/lindes/pubbin.git ~/lindes-bin
# And then *something like* the following.  (This may work verbatim, and
# may not.  AND, it may or may not be what you want, depending on how
# much you customize the environment you run in.  But it's probably
# (hopefully) workable for most folks.):
echo 'export PATH="$PATH:$HOME/lindes-bin/"' >> ~/.${SHELL#/bin/}rc
```

## Current contents:

* `ask` - prompt for a simple yes/no answer, loop and provide exit
  status to indicate response.

* `bigfiles` - a (very) simple wrapper around `mdfind` (a MacOS thing)
  and `du` to report on large files in the user's home directory.

* `fatsync` - a *very* simple wrapper around `rsync` to make it more
  friendly to
  [FAT](https://en.wikipedia.org/wiki/File_Allocation_Table)
  filesystems.

* `fixvt` - simple script to revert to a regular character set when
  some program or action (perhaps running `cat` on a binary file) has
  inadvertently switched your terminal into the VT100 character set
  intended for drawing on-screen forms.

* `gen-protractor-pdfs` - generate a PDF of a 360°
  [protractor](https://en.wikipedia.org/wiki/Protractor) for printing

* `git-initremote` - initialize a remote git repository (useful for
  when you're creating a new repo to push to - creates a bare repo
  according to a remote-spec already added with `git remote add ...`.)

* `is_plaintext` - check to see if a file (or files, and/or standard
  input) is "plain text" -- uses `file --mime-type` to figure that out.

* `jinja2` - a simple command-line front-end for checking jinja2 templates.

* `lispscript` - a shebang (`#!`) line interpreter to allow for easy
  creation of common-lisp scripts (using sbcl and quicklisp, with
  a pre-built startup ("core") file, for speedy startup.)

* `multiping` - ping multiple hosts and report a table of color-coded
  results.

* `not` - negates the exit-status meaning of a command, thus making
  possible things like `while not such-and-such; do sleep 1; done`,
  which will wait for such-and-such to return true.

* `toggle-pi-ap-mode` - toggles Access Point mode on a Raspberry Pi
  (with the help of some initial setup)

* `vagrant-rebox` - repackages a vagrant instance as a new box for
  vagrant, which can then be used as a baseline that's likely closer to
  your expected starting point, thus requiring less work (and less time
  spent) in the provisioning phase.

## License

All programs within this git repository are free software: you can
redistribute and/or modify them under the terms of the GNU General
Public License as published by the Free Software Foundation; either
version 3 of the License, or (at your option) any later version.

These programs are distributed in the hope that they will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

You should have received a copy of the GNU General Public License along
with this program.  If not, see <http://www.gnu.org/licenses/>.
