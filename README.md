# oper544

In 'Advanced Graphing', you may need to edit the way to apply a custom formatting function, depending on your version of Matplotlib:

Change this:

    # tell Matplotlib to use our custom formatter when drawing the tick labels
    ax.xaxis.set_major_formatter(format_xticks);
    
to this:

    # tell Matplotlib to use our custom formatter when drawing the tick labels
    from matplotlib.ticker import FuncFormatter
    xformatter = FuncFormatter(format_xticks)
    ax.xaxis.set_major_formatter(xformatter);

