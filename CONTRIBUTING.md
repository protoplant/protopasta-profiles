# Protopasta Filament Profile Changes

**_This repository is not the source of truth for Protopasta filament profiles._**

Protopasta filament profiles are _auto-generated_ from an online [Google Spreadsheet located here](https://docs.google.com/spreadsheets/d/17Ib1nh1-YTnJDln64uRwPn6WLWkjWtcKStA-Aes0ihk/edit?usp=sharing). This spreadsheet is considered the "Source of Truth" for all settings.

When changes are made, they are processed within this repository that generates a new Release with the required data.

## Processing Changes

This repository holds the source code that:

1. Monitors for changes to this spreadsheet
2. Downloads all changes for processing
3. Runs scripts on a per-slicer basis that generates the profiles
4. Creates a new Release
5. Attaches all profiles that generated successfully

This is all automated by Github Actions, located in [.github](.github), that calls individual build scripts. Those scripts are located in the root `slicers/` directory, for each slicer respectfully.

## Contributing

Contributions are welcome to the source code used to auto-generate the profiles, and for any new slicers.

Just open a Pull-Request against the `master` branch.
