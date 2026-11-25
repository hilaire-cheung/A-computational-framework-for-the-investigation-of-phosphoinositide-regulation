# A computational framework for the investigation of phosphoinositide regulation

Supplementary code and supporting files for the paper:

Cheung, H.Y.F., Tantiwong, C., Kale, D., Gibbins, J.M., Watson, S.P.,
Heemskerk, J.W., Sickmann, A., Ahrends, R. and Dunster, J.L. (2025).
“A computational framework for the investigation of phosphoinositide
regulation.” *PLOS Computational Biology*, 21(9), e1013477.
[https://doi.org/10.1371/journal.pcbi.1013477](https://doi.org/10.1371/journal.pcbi.1013477)

H.Y.F. Cheung is the first author; J.L. Dunster is the last and corresponding
author.

## Code provenance

The code in this repository is based on the
[PPI-Models repository](https://github.com/cardiomaths/PPI-Models). This
repository brings together the notebook and supporting files used with the
paper cited above. Refer to the PPI-Models repository for the upstream source
and its development history.

## Contents

- `NotebookPhosphoPSimulations.Rmd` — R notebook for simulating and plotting
  the models.
- `data/` — experimental data read by the notebook.
- `parameterSets/` — posterior parameter sets for the models.

## Requirements and running the notebook

The notebook was written and tested with R 4.3.2 and uses the `tidyr`,
`ggplot2`, `plyr`, `ggpubr`, and `deSolve` packages. Install any missing
packages in R with:

```r
install.packages(c("tidyr", "ggplot2", "plyr", "ggpubr", "deSolve"))
```

In RStudio, open `NotebookPhosphoPSimulations.Rmd` with the repository root as
the working directory. In the setup chunk, choose a `ModelName` matching a
parameter-set file in `parameterSets/` (for example, `A0` or `A01`), configure
the inhibitor settings if needed, and run the notebook. With `plotOutput` set
to `"Y"`, the notebook saves the figures in the working directory. By default,
it plots the first three simulations from the selected best-fit parameter set
to reduce computation time.

The paper describes the scientific methods and model details. The notebook and
the bundled data and parameter sets provide the files needed to run these
simulations.

## License

See [LICENSE](LICENSE) for this repository's license. Please also consult the
upstream PPI-Models repository for any applicable source-code notices or
attribution requirements.
`