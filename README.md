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

## Current contents:

* `fixvt` - simple script to revert to a regular character set when
  some program or action (perhaps running `cat` on a binary file) has
  inadvertently switched your terminal into the VT100 character set
  intended for drawing on-screen forms.

* `git-initremote` - initialize a remote git repository (useful for
  when you're creating a new repo to push to - creates a bare repo
  according to a remote-spec already added with `git remote add ...`.)

* `jinja2` - a simple command-line front-end for checking jinja2 templates.

* `not` - negates the exit-status meaning of a command, thus making
  possible things like `while not such-and-such; do sleep 1; done`,
  which will wait for such-and-such to return true.

* `toggle-pi-ap-mode` - toggles Access Point mode on a Raspberry Pi
  (with the help of some initial setup)

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
