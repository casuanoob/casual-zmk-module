## Instructions

Add this repository to your existing `config/west.yml` as shown below. (No idea what that means? [Make a new repo from this template first](https://github.com/zmkfirmware/unified-zmk-config-template), and [go read the docs](https://zmk.dev/docs/customization#building-additional-keyboards)!)

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    # Add the base GitHub URL as a remote.
    - name: casuanoob # You can name this whatever you like; just make sure the "remote" below matches.
      url-base: https://github.com/casuanoob
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    # Add the name of the repository as a project.
    - name: casual-zmk-module
      remote: casuanoob
      revision: main # This is the name of the branch you want to use.
  self:
    path: config
```

After making this change, copy any keymaps you may need out of the appropriate board and/or shield folders and paste them into your `config` folder for later modification. Don't forget to [edit your `build.yaml` to include them](https://zmk.dev/docs/customization#building-additional-keyboards), too.

## Current shields

- [Charybdis 4x6 v2](https://github.com/Bastardkb/Charybdis)
  - n!n build with v2 shield ***only***. No trackball support on this. It is highly unlikely your build is compatible with this, and if you don't understand this dotpoint then *do not use this*.
- [Luna](https://github.com/mindhatch/keyboards?tab=readme-ov-file#%E3%83%AB%E3%83%8A-luna)
- [Rollow](https://github.com/barbellboards/Rollow)
  - OLED support is untested because I don't have one on my build, but it's copy-pasted from upstream corne (as is nearly all of the config) so it should work.
  - The five_column_transform works and I have tested this
  - The default 6col transform should work but I have not tested it because I have the 5col version only.
- [Skeletyl v2](https://github.com/Bastardkb/Skeletyl)
  - n!n build with v2 shield ***only***. If you don't understand what that means, *do not use this*.
