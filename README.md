# zone-matrix

These files were taken from [ober's zone-matrix repo](https://github.com/ober/zone-matrix) but the original is available at [Dylan Wen's dot-emacs repo](https://github.com/hhkbp2/dot-emacs) specifically the [dot-emacs/site-lisp/misc/zone](https://github.com/hhkbp2/dot-emacs/tree/acf11eb4f1bac643f5eccb1abdb1647f0d022b3c/site-lisp/misc/zone) directory.

I attempted to do a little tidy up, nothing major just to get it all neatly centered in one file, remove some of the use package stuff and advice.  All the original work that actually means something is by Dylan Wen and ober.

You should be able to clone this into your emacs directory somewhere in the `load-path` and then use `use-package` on it.  If your `load-path` needs setting then:

```
(add-to-list 'load-path (expand-file-name "~/.emacs.d/path/to/zone-matrix"))
```

Then you can load it with a regular `use-package` call, this example sets it as the only zone-program and also starts it after 60 seconds of idle time.

```
(use-package zone-matrix
  :config
  (setq zone-programs [zone-matrix])
  (zone-when-idle 60))
```

Then just calling `M-x zone` should give you a lovely matrix zone.  Probably works better on darker background themes.

In case anything else needs bodging in future I added two hooks `zmx-before-hook` and `zmx-after-hook` so users can readily add their own little tweaks.


# Original README

These files are take from Dylan Wen's dot-emacs repo at:

https://bitbucket.org/lisp/dot-emacs

He is the author of these files and I merely just packaged this up so that I could easily have access to it.
![zone-matrix](https://user-images.githubusercontent.com/169890/232936153-eb07612f-0bd4-4edd-acc8-983f76f0f98e.png)
