.. _index

.. lets-plot documentation master file, created by
   sphinx-quickstart on Fri May 15 17:50:59 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. include:: /shared/previews.rst


Explore Your Data with Lets-Plot
================================

.. panels::
    :container: + previews-slider-window id-1
    :column: col-lg-1 p-2

    .. image:: _static/images/slider_left.png
        :target: #

    ---
    :column: col-lg-10 p-2

    |map_airports_4x3-kaggle|

    ---
    :column: col-lg-1 p-2

    .. image:: _static/images/slider_right.png
        :target: #

.. panels::
    :container: + previews-slider-content id-1 hidden
    :column: col-lg-3 col-md-4 col-sm-6 col-xs-12 p-2

    |map_airports-kaggle|

    ---
    |geom_smooth_matrix-nbviewer|

    ---
    |geopandas_kotlin_isl-nbviewer|

    ---
    |formatting_axes_etc-nbviewer|

.. panels::
    :column: col-lg-4 col-md-4 col-sm-6 col-xs-12 p-2

    Grammar of Graphics
    ^^^^^^^^^^^^^^^^^^^

    .. raw:: html

        <a class="reference internal image-reference" href="pages/gog.html">
          <img src="_images/graph_building.png">
        </a>
        <br/>
        <br/>

    The **Lets-Plot** for Python library includes a native backend and a :ref:`Python API <api>`, which was mostly based on the `ggplot2 <https://ggplot2.tidyverse.org>`__ package well-known to data scientists who use R.

    ---
    Interactive Maps
    ^^^^^^^^^^^^^^^^

    .. raw:: html

        <a class="reference internal image-reference" href="pages/interactive_maps.html">
          <img src="_images/museums.png">
        </a>
        <br/>
        <br/>

    **Lets-Plot** supports interactive maps via the ``geom_livemap()`` geom layer which enables a researcher to visualize geospatial information on a zoomable and paneble map.

    ---
    Hot Features
    ^^^^^^^^^^^^

    .. raw:: html

        <a class="reference internal image-reference" href="pages/features.html">
          <img src="_images/scatter_matrix.png">
        </a>
        <br/>
        <br/>

    With **Lets-Plot** you got an access to the bunch of high-level features that help you to build beautiful plots with ggplot-like API.

Installation Guide
------------------

.. panels::
    :column: col-lg-6 col-md-4 col-sm-6 col-xs-12 p-2

    For Linux and Mac users
    ^^^^^^^^^^^^^^^^^^^^^^^

    To install the **Lets-Plot** library, run the following command:

    .. code:: shell

        pip install lets-plot

    ---
    For Windows users
    ^^^^^^^^^^^^^^^^^

    Install Anaconda3 (or Miniconda3), then install MinGW toolchain to Conda:

    .. code:: shell

        conda install m2w64-toolchain

    Install the **Lets-Plot** library:

    .. code:: shell

        pip install lets-plot

Quickstart with Jupyter
-----------------------

You can use **Lets-Plot** in a Jupyter notebook or another notebook of your choice, like Datalore, Kaggle or Colab.

To evaluate the plotting capabilities of **Lets-Plot**, add the following code to a Jupyter notebook:

.. jupyter-execute::
    :linenos:

    import numpy as np
    from lets_plot import *
    LetsPlot.setup_html()        

    np.random.seed(12)
    data = dict(
        cond=np.repeat(['A','B'], 200),
        rating=np.concatenate((np.random.normal(0, 1, 200), np.random.normal(1, 1.5, 200)))
    )

    ggplot(data, aes(x='rating', fill='cond')) + ggsize(500, 250) + \
        geom_density(color='dark_green', alpha=.7) + scale_fill_brewer(type='seq') + \
        theme(axis_line_y='blank')

.. raw:: html

    <div class="lets-plot-platforms">
      <div>
        <a class="reference external" href="https://nbviewer.jupyter.org/github/JetBrains/lets-plot/blob/master/docs/examples/jupyter-notebooks/quickstart.ipynb">
          <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" />
        </a>
      </div>
      <div>
        <a class="reference external" href="https://view.datalore.io/notebook/Zzg9EVS6i16ELQo3arzWsP">
          <img src="https://raw.githubusercontent.com/JetBrains/lets-plot/master/docs/examples/images/logo_datalore.svg" />
        </a>
      </div>
      <div>
        <a class="reference external" href="https://plugins.jetbrains.com/plugin/14379-lets-plot-in-sciview">
          <img src="_static/images/logo/icon-pycharm.svg" />
        </a>
      </div>
      <div>
        <a class="reference external" href="https://www.kaggle.com/alshan/lets-plot-quickstart">
          <img src="https://raw.githubusercontent.com/JetBrains/lets-plot/master/docs/examples/images/logo_kaggle.svg" />
        </a>
      </div>
      <div>
        <a class="reference external" href="https://colab.research.google.com/drive/1uYYZcG0g0kP4lJdPkpWB8aBS96ioDii2?usp=sharing">
          <img src="https://raw.githubusercontent.com/JetBrains/lets-plot/master/docs/examples/images/logo_colab.svg" />
        </a>
      </div>
      <div>
        <a class="reference external" href="https://deepnote.com/project/673ea421-638e-469d-8d04-5cc4c6e0258f#%2Fnotebook.ipynb">
          <img src="https://raw.githubusercontent.com/JetBrains/lets-plot/master/docs/examples/images/logo_deepnote.svg" />
        </a>
      </div>
    </div>

Quickstart with Datalore
------------------------

You can try the **Lets-Plot** library in `Datalore <https://datalore.jetbrains.com>`__. **Lets-Plot** is available in Datalore out-of-the-box.

The advantage of `Datalore <https://datalore.jetbrains.com>`__ as a learning tool in comparison to Jupyter is that it is equipped with a very friendly Python editor which comes with auto-completion, intentions and other useful coding assistance features.

Begin with the `quickstart in Datalore <https://view.datalore.io/notebook/Zzg9EVS6i16ELQo3arzWsP>`__ notebook to learn more about Datalore notebooks.

.. raw:: html

    <div class="video-container">
      <iframe width="640" height="360" src="https://www.youtube.com/embed/MjvFQxqNSe0"></iframe>
    </div>

More Examples
-------------

.. panels::
    :container: + preview-gallery
    :column: col-lg-3 col-md-4 col-sm-6 col-xs-12 p-2

    |beijing-kaggle|

    ---
    |correlation_plot-nbviewer|

    ---
    |geocoding_examples-nbviewer|

    ---
    |ggbunch-nbviewer|

    ---
    |geopandas_naturalearth-nbviewer|

    ---
    |image_matrix-nbviewer|

    ---
    |plotting_airbnb_prices_boston-datalore|

    ---
    |tooltip_config-nbviewer|

    ---
    |sampling_groups-nbviewer|

    ---
    |sampling_pick-nbviewer|

    ---
    |sampling_stratified-nbviewer|

    ---
    |sampling_vertex-nbviewer|

.. raw:: html

    <div id="preview-gallery-more">
      <a href="pages/gallery.html" class="reference internal">Show More</a>
    </div>