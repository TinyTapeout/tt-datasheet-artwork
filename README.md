# Tiny Tapeout Datasheet Artwork

This repo is intended to provide easy access to artwork which is dedicated to Tiny Tapeout. Its contents are used by the
shuttle "build datasheet" action to showcase photos and renders from the team and community.

Details of each photo (such as its title and artist) can be found within the `manifest.yaml` file. New photos must be
added to `manifest.yaml` and the required fields filled out so that the build action can make use of the images.

## Structure of `manifest.yaml`

The manifest can contain multiple root keys, such as `artwork`, which correspond to a folder within the repo.

These root keys then contain multiple key-value pairs which are used fetch information like the artist, designer,
actual file of the image and its title. Each key must be unique, as that is used to ID it.

Example:
```yaml
artwork:
    image_1:
        title: Chip Decap
        designer: Person A
        artist: Person B
        file: decap.jpg
```

In this example, `image_1` (its unique ID) should live at `artwork/decap.jpg`.