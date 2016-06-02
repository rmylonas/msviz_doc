
.. Non-breaking white space, to fill empty divs
.. |nbsp| unicode:: 0xA0
   :trim:


.. warning:: **Browser compatibility**: MsViz was tested with **Firefox** (46.0.1), **Google Chrome** (50.0.2661) and **Safari** (9.1.1). MsViz is currently not compatible with Internet Explorer.

Users' manual
=============

.. figure:: /images/msviz_searches.png
   :width:  100%
   :alt: Main window

1.  :ref:`searches`: compare or delete existing data.
2.  :ref:`uploads`: upload new datasets or databases.
3.  :ref:`resultBasket`: look at data you added to your result basket.


.. _searches:

Searches
-------------

Select searches
.................

.. figure:: /images/msviz_select_searches.png
   :width:  100%
   :alt: Select searches


Select the checkboxes of the *SearcheIds* you want to compare. Click on the *Compare* button to see all the proteins identified in the selected searches.

Compare searches and select protein
...............

.. figure:: /images/msviz_proteins.png
   :width:  100%
   :alt: Select proteins

The order of the searches can be re-arranged by simple drag-and-drop. This feature is useful to group together searches which share the same experimental condition. 

You can filter the list of proteins by choosing a post translational modification (PTM) of interest. Only the proteins containing this PTM will be kept.

Select a protein to switch to the :ref:`detail view <protein_coverage>`.

.. _protein_coverage:

Protein coverage view
......................

.. figure:: /images/msviz_protein_coverages.png
   :width:  100%
   :alt: Protein coverages

The coverages of the selected proteins are shown as green bars. The thickness of the bars correspond to the spectral counts for each peptide. 

You can get more information about the amino acid sequence by moving with the mouse pointer over the graph. With a mouse-click on the green bars you get the :ref:`psm_details` for the selected position. 

Post Translational Modification (PTM) counts
..............................................

.. figure:: /images/msviz_psm_count.png
   :width:  100%
   :alt: PSM counts

By selecting a PTM from the drop-down menu you can see the positions with modifications as blue circles (only for the experimental data). The size of the blue circles corresponds to the spectral count containing the selected modification.

On top of the graph you can see labels indicating the modified amino acids (one letter code) together with their position. By clicking on either the labels or the blue circles you get the :ref:`psm_details` for the selected position.

.. figure:: /images/msviz_zoom_region.png
   :width:  70%
   :alt: PSM zoom

You can zoom into a region by seleting an area with your mouse (press left button, select a region and release the button). The zoom can be reset with a double-click of the left mouse button in any empty area. 


.. _psm_details:

Peptide Spectrum Match (PSM) details
......................................

.. figure:: /images/msviz_ptms.png
   :width:  100%
   :alt: PSM details

Every PSM is represented by a gray line. By moving your mouse over the PSM's you can see a popup showing  information about the match (scan number, retention time, charge, precursor mass, AA sequence together with modifications and scores). 

On the PSM's you can see the selected PTM's represented by circles: 

- Red circles show the most probable PTM positions. By "most probable" we mean the PTM positions found in the highest ranking PSM.

- Orange circles indicate a conflicting position. This means the position was found in a lower ranking PSM, but which has the same identification score as the highest ranking one.

- Gray circles show PTM positions of lower ranking PSM's.

- Other modifications then the selected one are shown as black bars.

By clicking on any PSM you open a :ref:`detail view <detail_view>` showing the corresponding :ref:`fragmentation spectrum <spectrum_details>` and :ref:`XIC's <xic_view>`. 


.. _detail_view:

Visualization of spectra and XIC's
....................................

.. figure:: /images/msviz_details.png
   :width:  100%
   :alt: spectra and XIC details

By clicking on an PSM (gray lines) you open a view to the corresponding :ref:`annotated fragmentation spectrum <spectrum_details>` and :ref:`XIC's <xic_view>`. This allows to easily verify the quality of the match and quantify the corresponding MS1 signals. 

1. :ref:`spectrum_details`: the annotated fragmentation spectrum helps you to verify the quality of the match.

2. :ref:`xic_view`: quantify the corresponding MS1 signal.

3. Alternative matches: look at alternative matches for this spectrum. 

.. _spectrum_details:

Annotated fragmentation spectrum
..................................

.. figure:: /images/msviz_spectrum.png
   :width:  100%
   :alt: spectrum details

The spectrum shows annotated peaks with B-ions in blue and Y-ions in red. You can zoom into a region by selecting an area with your mouse (left button). 

To compare all opened fragmentation spectra amongst each other, you can click on the **magnet button**. This sets the mass range of all other spectra to the one from which you clicked. The zoom can be reset by clicking on the **reload button** by double-clicking on any empty area of the graph.

The **zoom button** opens the corresponding spectrum and XIC in an extra browser tab. You get a bigger view of both graphs. That is useful for looking at details and to make prettier screenshots.

.. _xic_view:

Extracted Ion Chromatogram (XIC) 
.................................

.. figure:: /images/msviz_xic.png
   :width:  100%
   :alt: xic

The XIC is generated by extracting the MS1 signal of the given mass over charge (m/z) ratio and a **tolerance of 10 ppm**. 

Again, to compare all XIC's amongst each other, you can click on the **magnet button**. This sets the retention-time range of all other XIC's to the one from which you clicked. The zoom can be reset by clicking on the **reload button** or by double-clicking on any empty area of the graph.

Spectra and XIC's can be closed by clicking on the **close button**.

.. figure:: /images/msviz_xic_quanti.png
   :width:  100%
   :alt: xic quantitation

You can quantitate the XIC peaks by selecting a region. To do so you select an area, like done for zooming, but in this case you hold down the **SHIFT** key while selecting. A green area while show the region were the quantitation was done and a table containing intensity values will appear below.

The quantitation table shows the maximum intensity for the region of interest (*Intensity*) and the exact retention time where this intensity was found (*Rt*). This information can be added to the :ref:`resultBasket` by clicking on the **basket button**.

.. _uploads:

Uploads
-------------

.. warning:: The upload and delete functions are disabled for the `public MsViz <http://msviz-public.vital-it.ch/>`_. 

Upload results
.................

.. figure:: /images/msviz_uploadResults.png
   :width:  100%
   :alt: Upload results

The types of data currently accepted by MsViz are either Mascot or MaxQuant results.

Select the file to upload. It has to be a *.zip* file containing:

- **Mascot**: All the *.MzML* files used for MS1 and MS2 acquisition and *.mzid* file with identification results.

- **MaxQuant**: All the *.MzML* files used for MS1 and MS2 acquisition and the folder called */txt* with identification results.

By clicking the **Upload button** your file will be loaded on MsViz.


Upload database
.................

.. figure:: /images/msviz_uploadDatabase.png
   :width:  100%
   :alt: Upload database

The database accepted by MsViz has to be a *.fasta* file.

By clicking the **Upload button** your file will be loaded on MsViz.

You can see a list of the databases you already loaded.

.. _resultBasket:

Result Basket
-------------

.. figure:: /images/msviz_resultsBasketBoth.png
   :width:  100%
   :alt: Results basket

By clicking on any of the results in the list you open a view to the selected one.

You can remove your results or you can export them into a *.csv* containing the protein AC, the peptide, scan number, retention time, m/z, charge, score and intensity for all your samples. 




