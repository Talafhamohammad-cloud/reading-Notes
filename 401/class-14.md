# matplot:
matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats. We are going to explore matplotlib in interactive mode covering most common cases.

## IPython and the pylab mode:
IPython is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more. When we start it with the command line argument -pylab (--pylab since IPython version 0.12), it allows interactive matplotlib sessions that have Matlab/Mathematica-like functionality.

## pyplot:
pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM). Therefore, the majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments. Important commands are explained with interactive examples.

## seaborn tutorial:
Seaborn is a library for making statistical graphics in Python. It is built on top of matplotlib and closely integrated with pandas data structures.
some of the functionality that seaborn offers:

1- A dataset-oriented API for examining relationships between multiple variables
2- Specialized support for using categorical variables to show observations or aggregate statistics
3- Options for visualizing univariate or bivariate distributions and for comparing them between subsets of data
4- Automatic estimation and plotting of linear regression models for different kinds dependent variables
5- Convenient views onto the overall structure of complex datasets
6-High-level abstractions for structuring multi-plot grids that let you easily build complex visualizations
7- Concise control over matplotlib figure styling with several built-in themes
8- Tools for choosing color palettes that faithfully reveal patterns in your data
9- Figures, Subplots, Axes and Ticks

So far we have used implicit figure and axes creation. This is handy for fast plots. We can have more control over the display using figure, subplot, and axes explicitly. A figure in matplotlib means the whole window in the user interface. Within this figure there can be subplots. While subplot positions the plots in a regular grid, axes allows free placement within the figure. Both can be useful depending on your intention. We???ve already worked with figures and subplots without explicitly calling them. When we call plot, matplotlib calls gca() to get the current axes and gca in turn calls gcf() to get the current figure. If there is none it calls figure() to make one, strictly speaking, to make a subplot(111). Let???s look at the details.

## Figures:
A figure is the windows in the GUI that has ???Figure #??? as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. This is clearly MATLAB-style.

## Subplots:
With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.

## Ticks:
Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks. There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other. By default minor ticks are not shown, i.e. there is only an empty list for them because it is as NullLocator

## Animation
For quite a long time, animation in matplotlib was not an easy task and was done mainly through clever hacks. However, things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, with the possibility to save them in all kind of formats (but don???t expect to be able to run very complex animations at 60 fps though).
