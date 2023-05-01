# Simple Linear Regression

## How to run

Install the TAF package from CRAN. Then open R in the `taf-demo` directory and
run:

```
library(TAF)
taf.boot()
source.all()
```

## Explore results

After running the analysis, we get plots and formatted tables in the final
`report` folder, to paste into a report. The entire analysis is scripted and the
results can be traced back to the initial data and through the analytical steps
in the TAF scripts.

---

## Quick intro to TAF

The initial data are declared in [DATA.bib](boot/DATA.bib), which is processed
by the `taf.boot()` function. During this boot procedure, each metadata entry is
processed and the TAF system then makes the data available in the `boot/data`
folder, where the `data.R` script will read it.

After the boot procedure, the `data.R`, `model.R`, `output.R`, and `report.R`
scripts are run sequentially, each picking up files from previous steps. See the
general [TAF flow
diagram](https://github.com/ices-taf/doc/blob/master/simple.pdf).

The purpose of each script is indicated in the header comments:

Script     | Purpose
---------- | ----------------
`data.R`   | Preprocess data
`model.R`  | Run analysis
`output.R` | Extract results
`report.R` | Plots and tables

TAF provides a way to divide any analysis into these four main steps. In
addition to supporting reproducibility, the standardized structure makes
analyses more manageable and reviewable.

## See also

- [ICES TAF landing page](https://taf.ices.dk)
- [ICES TAF documentation](https://github.com/ices-taf/doc)
- Tutorial [video](https://www.youtube.com/watch?v=FweJbr9hfdY) and [annotated
  transcript](https://github.com/ices-taf/doc/tree/master/tutorial-1#readme)
- [TAF package](https://cran.r-project.org/package=TAF) help pages
- ICES TAF stock assessment examples:
  - [2015 Spotted ray](https://github.com/ices-taf/2015_rjm-347d) in the Eastern
    Channel
  - [2015 Haddock](https://github.com/ices-taf/2015_had-iceg) in Icelandic
    waters
  - [2016 Plaice](https://github.com/ices-taf/2016_ple-eche) in the Eastern
    Channel
  - [2016 Cod](https://github.com/ices-taf/2016_cod-347d) in the North Sea
  - [2019 Sandeel](https://github.com/ices-taf/2019_san.sa.6) in Area 6
