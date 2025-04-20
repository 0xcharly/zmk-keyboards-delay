# Personal ZMK Module

This repository contains the shield files for the keyboard that I'm using.

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the
`0xcharly` module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: 0xcharly
      url-base: https://github.com/0xcharly
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboards-delay
      remote: 0xcharly
      revision: main
  self:
    path: config
```

Once you have the module added to your west.yml you can then build firmware as
if it was in your config's shield directory or in ZMK main.
