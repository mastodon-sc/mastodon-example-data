# mastodon-example-data

This repository contains example datasets for the Mastodon cell-tracking plugin.

## Dataset: tgmm-mini
### Origin
This dataset was created from the example dataset released with the TGMM software
(https://www.janelia.org/lab/keller-lab/software/fast-accurate-reconstruction-cell-lineages-large-scale-fluorescence).

The image data was converted from TIFs into BigDataViewer HDF5/XML.
The tracks were imported from TGMMs XML output files into Mastodon.

### License
(see also [tgmm-mini/LICENSE.txt](tgmm-mini/LICENSE.txt))

Janelia Open-Source Software
Copyright © 2018 Howard Hughes Medical Institute

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
Neither the name of HHMI nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS “AS IS” AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## Dataset: astec

### Origin

* This dataset originates from the Phallusia mammillata embryonic development dataset, which was published on
  figshare.
    * https://figshare.com/projects/Phallusiamammillata_embryonic_development/64301.
* The dataset is described in the following publication:
    * Léo Guignard et al., Contact area–dependent cell communication and the morphological invariance of ascidian
      embryogenesis. Science369, eaar5663(2020). DOI:[10.1126/science.aar5663](https://doi.org/10.1126/science.aar5663)
* The dataset has been converted to Mastodon file format using these scripts:
    * Astec file format to CSV: https://github.com/leoguignard/LineageTree/tree/master/src/LineageTree/export_csv.py
    * CSV to Mastodon file
      format: https://github.com/mastodon-sc/mastodon-deep-lineage/blob/master/src/test/java/org/mastodon/mamut/astec/AstecReader.java
* Limitations resulting from the conversion:
    * Image data is not included in the projects. This would require additional effort. However, it is probably not
      necessary
      for the intended use cases (tests of lineage clustering, lineage registration, and Blender visualization).
    * Only datasets Pm01 – Pm10 have been converted.
    * The cell names were missing for Pm11-Pm13. To handle this, the conversion scripts would need to be adapted. Thus,
      these datasets are not included.
    * The uploaded data for Pm14 is faulty on figshare. Thus it is not included.
    * Half-Pm1, U0126PM1 and U0126PM2 do not contain lineage or coordinates. Thus, these datasets are not included.
    * When opening the Mastodon projects, a message appears stating that the image data is missing. It can be chosen, to
      open the project without image data ("dummy image data"). This must be confirmed. After that, it should work.

### License

(see also [astec/LICENSE.txt](astec/LICENSE.txt))

* The data is licensed under CC-BY 4.0: https://creativecommons.org/licenses/by/4.0/
