# latex-template-fhv
My own template for a latex thesis.

To use:
1. Replace all full paths inside main.tex with your own
   1. Minted package: outputDir must point to the auxil folder
   2. Python script path `\renewcommand{\MintedPygmentize}{<path>}`: Path to the pygmentize script location
2. Compile the main.tex file with pdfLatex.</br>
  Example (you have to change the paths):
    ```shell
    pdflatex 
      -file-line-error 
      -interaction=nonstopmode 
      -synctex=1 
      -output-format=pdf 
      -output-directory=Z:/Users/jan22/CodeProjects/latex_template/out 
      -aux-directory=Z:/Users/jan22/CodeProjects/latex_template/auxil 
      -include-directory=Z:/Users/jan22/CodeProjects/latex_template/src 
      -shell-escape 
      --max-print-line=140 
      main.tex
    ```
    
3. If you use Intellij IDEA you might want to check out the plugin Texify [Plugin Page](https://plugins.jetbrains.com/plugin/9473-texify-idea)
Just add -shell-escape --max-print-line=140 to additional cl inputs field.
