# tryhisto

I wanted to make histograms, log scale preferred.

Why was it so hard?

C.f. http://johnj.com/nucleotide-repetition-lengths.html

This repo provides a more up-to-date version of that.

## Coordinates

    [eigenhombre/logplots "0.0.1"]

## Example

    (require '[logplots.histo :as h])
    (->> #(apply + (repeatedly 100 rand))
           (repeatedly 10000)
           (concat (repeatedly 1000 #(rand-int 400)))
           (make-hist 10 100 100)
           (draw-hist "Gaussian-ish, log" true))

![Example](doc/example.png)

## License

Copyright © 2019 John Jacobsen

This program is free software. It comes without any warranty, to
the extent permitted by applicable law. You can redistribute it
and/or modify it under the terms of the Do What The F~~~ You Want
To Public License, Version 2, as published by Sam Hocevar. See
yhttp://www.wtfpl.net/ for more details.
