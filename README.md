# Extro.py

Extro.py reads dependency information from a set of directories and
produces an ordered listing of this directories.

## Specifying dependency information

Extro.py looks for dependency information inside the `.deps` directory of
each named directory.  Inside the `.deps` directory it will read
information from the following files:

- `requires` -- Names (basename only, not paths) of directories
  required by this directory.
- `required_by` -- This is a reverse `requires`.  If `dir1` is
  *required_by* `dir2`, that is the same as if `dir2` had listed `dir1`
  in its `requires` file.
- `provides` -- a list of aliases that can be used to refer to the
  current directory.

## License

extro.py -- imposes an ordering on a list of directories  
Copyright (C) 2016 Lars Kellogg-Stedman <lars@oddbit.com>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
