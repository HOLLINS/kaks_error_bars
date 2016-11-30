**Description** 

The [R script][3] (./plot_kaks_err_bars.R), calculates error bars for dN/dS (a.k.a Ka/Ks) values, calculated for pairs of orthologous DNA sequences. The dN/dS values have to already be calculated by the [KaKs calculator][2], who will make an outputfile, only then can ./plot_kaks_err_bars.R be able to generate the error bars (see below for instructions/requirements). 

To help you explore your data, ./plot_kaks_err_bars.R will also make barplots of your dN/dS (a.k.a Ka/Ks) values, adding the error bars onto the barplot. Y-axis is dN/dS and each bar on the X-axis is a different pair of DNA sequences.  

---
 
**Requirements / How to use**

For this dish, You WILL need the following ingredients: 

 1. The [KaKs calculator][2] (read installation instructions: ), it's output data is what this R script (./plot_kaks_err_bars.R) needs for error bar generation. 

 2. A pair (or multiple pairs) of [orthologous][1] DNA sequences in a format that [KaKs calculator][2] accepts, e.g. ./example_kaks_calc_output.txt has several pairs of HTLV-1 viral gene sequences' dN/dS data (each pair has one ortholog for HTLV-1 and one ortholog for STLV-1 virus). To be more specific you might need each pair of orthologous sequences to be already aligned, read the docs for KaKs Calculator if you are not sure.  

 
---

You MIGHT also need:

 1. Windows (OR ubuntu)

 2. RStudio IDE, it's free (I have not used on any other IDE, maybe you don't need)

 3. Latest version of R (Only tested on 2014+ versions)

---

You need to then follow this recipe: 

 1. Run the KaKs calculator (https://code.google.com/archive/p/kaks-calculator/), read the instructions and give the DNA sequences it needs

 2. Run this R script (./plot_kaks_err_bars.R), it will then prompt you for a data file (next step)

 3. Browse for your KaKs calculator output file, select it then click. There might be several output files, so here I have an example data file that you can use as a reference, it SHOULD work: ./example_kaks_calc_output.txt

 4. All done! The plot can be shown interactively, or uncomment CTRL+F: "@PLOT" line in the script to save to .PNG file kaks_error_bars

---

If you find that something does not work, or you see a conceptual issue with the code please do not hesitate to make a message on the GitHub repo. 


[1]: http://homepage.usask.ca/~ctl271/857/def_homolog.shtml
[2]: https://code.google.com/archive/p/kaks-calculator/
[3]: https://github.com/a1ultima/kaks_error_bars/blob/master/plot_kaks_err_bars.R