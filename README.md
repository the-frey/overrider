# Overrider

A repo for the overrider project.

## Running

First, start supercollider by running this inside the repo:

    $ sclang superdirt_startup.scd

Then, head to emacs and `C-c C-s`.

You can use `C-RET` to eval within a `.tidal` file.

## Known issues

Some things don't work so well on linux.

Sometimes the tidal install doesn't quite gel, and you need to install with stack instead.

### Jack

After following the instructions on the tidal site, you'll probably still need to:

```shell
sudo apt-get install jackd2
sudo dpkg-reconfigure jackd2
sudo addgroup <yr-username> audio
```

It may be that this still doesn't work, and jack can't start.

This could be because it doesn't know which soundcard to use, so [follow the instructions here](http://dpod.kakelbont.ca/2015/08/16/fixing-qjackctl/) to fix it.

Essentially, run `qjackctl`, then on the 'Advanced' tab of settings, change input and output devices to `hw:PCH`.

### Emacs

You might need to follow [these instructions](https://github.com/tidalcycles/Tidal/issues/480), or crack and use atom.

Reinstalling the Haskell platform is a bit of a faff.
