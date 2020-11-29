# Overview
The other day I needed to reverse a hexdump produced by `hexdump -C`... `xxd -r` was flagged as the way to do it, but crazily enough in its documentation it stated that it didn't actually notify the user of parse errors... in effect there was no good way of ensuring that it was processing my hexdump!  Digging around more, I didn't find a canonical way of reversing a hexdump, so I decided to prepare my own utility.

I've borrowed heavily from the `reverse-hexdump.sh` script by ???.  So the core intellectual credit for this tool's functionality should definitely go to him.  Thanks!

## Known issues
  - Not heavily tested.

# Quick start

## Installation
This tool will run fine in pretty much any unix distribution.  It requires the following tools:
  - sh
  - awk

If you have these, just download it and run `sudo make install` to install it to `/usr/local/bin`.

## Usage

# Contributions
I don't work heavily with hexdumps, so I'm sure there will be gaps.  Any and all contributions are welcome.  See the (very mild) design guidelines below.  Just hit me up with a pull request.

## Design considerations
  - As much as possible, I'd like for `hexload` to mirror `hexdump` - so wherever possible, let's stick to using the same options and option semantics as possible.
  - Make sure that any functionality you add or fix are covered by unit tests (see examples under `tests`).  Since `hexload` is intended to be a mirror to `hexdump`, I'd expect that every test script will start with using `hexdump` to do something.
