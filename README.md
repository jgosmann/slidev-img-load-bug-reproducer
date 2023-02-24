# This is a quite minimal reproducer of a weird Slidev bug

To see it:

```shell
npm install
npm run dev
```

Then flip quickly through the slides.
On the last slide the "B" image won't load.
You can go back and forth and it still won't load.
If you reload on the "B" slide, the image will load.
But now going quickly back to the "A" slide will cause that image to no longer load.

If you load one of the intermediate slides first,
the first of the "A" or "B" slides you load will load its image,
but the image on the other slide (usually) does not load.

Opening the overview of all slides will cause both images to load.

Removing the intermediate slides makes it less likely that one of the images won't load.
There also seems to be some timing factor.
With fewer slides it seems that flipping quickly through them causes one of the images to not load,
while going more slowly will load both.

## Affected versions and system

* Slidev v0.40.0 seems to be **not** affected.
* Slidev v0.40.1 is affected (thus likely the earliest affected version).
* Slidev v0.40.3 is affected (latest version at point of discovery).
* Only occurs when using windicss, does not occur with unocss.
* Occurs both in Firefox and Chrome on macOS.
* Occurs only in dev mode, building a static version works fine.
