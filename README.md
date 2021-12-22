# Testing the Nix package manager

First, make sure you have installed the Nix package manager. The installation will ask you for your `sudo` password, so be sure to have it.

```sh
curl -L https://nixos.org/nix/install | sh
```

## Building and running

Running `nix-build` from within the directory. This will build based on what's defined in `default.nix` by default

```sh
nix-build
```

Once built, start a shell and run the test app, `myapp.py`

```sh
nix-shell default.nix
python3 myapp.py
```

This app can now only be ran from within the `nix-shell`. Try running it in your normal shell and see what happens

```sh
python3 myapp.py
```
