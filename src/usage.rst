
.. Non-breaking white space, to fill empty divs
.. |nbsp| unicode:: 0xA0
   :trim:

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

Select the checkboxes of the *SearcheIds* you want to compare. Click on the *Compare* button to see all the proteins identified in the selected searches.

Select protein
...............

.. figure:: /images/msviz_proteins.png
   :width:  100%
   :alt: Select proteins

The order of the searches can be re-arranged by simple drag-and-drop. This feature is useful to group together searches which share the same experimental condition. 

You can filter the list of proteins by choosing a post translational modification (PTM) of interest. Only the proteins containing this PTM will be kept.

Select the protein of interest to look at this protein in more detail. It will open the :ref:`protein_coverage`.

.. _protein_coverage:

Protein coverage view
......................

.. figure:: /images/msviz_protein_coverages.png
   :width:  100%
   :alt: Protein coverages

The coverages of the selected samples are shown as green bars. The thikness of the bars correspond to the number of PSM's at a position. 

By moving with the mouse pointer over the graph, you can get more information about the amino acid sequence. By clicking on the green bars you get the :ref:`psm_details` at the selected position. 

Post Translational Modification (PTM) counts
..............................................

.. figure:: /images/msviz_psm_count.png
   :width:  100%
   :alt: PSM counts

By selecting a PTM from the drop-down menu you can see the position of modifications as blue circles. The size of the blue circles corresponds to the number of PSM's containing the selected modification.

On the top you can see labels indicating the modified amino acid (one letter code) together with their position. By clicking on either the labels or the blue circles you get the :ref:`psm_details` at the selected position.

.. figure:: /images/msviz_zoom_region.png
   :width:  70%
   :alt: PSM zoom

You can zoom into a region of the graph by seleting an area with your mouse (press left button, selected a region and release the button). The zoom can be reset with a double-click of the left mouse button in any empty area. 


.. _psm_details:

Peptide Sepctrum Match (PSM) details
......................................

.. figure:: /images/msviz_ptms.png
   :width:  100%
   :alt: PSM details

Every PSM is represented by a gray line. By moving your mouse over the PSM's you can see a popup showing detail information (scan number, retention time, charge, precursor mass, sequence with modifications, identification and localisation scores). 

On the PSM's you can see the selected PTM's represented by circles: 

- Red circles show the most probable PTM positions. By "most probable" we mean the positions found in the highest ranking PSM.

- Orange circles indicate a conflicting position. This means that this position was found in a lower ranking PSM, which has the same identification score as the highest ranking one.

- Gray circles show PTM positions of lower ranking PSM's.

- Other modifications then the selected one are shown as black bars.

By clicking on any of the PSM's you open a :ref:`detail view <detail_view>` to the corresponding :ref:`fragmentation spectrum <spectrum_details>` and :ref:`XIC's <xic_view>`. 


.. _detail_view:

Visualization of spectra and XIC's
....................................

.. figure:: /images/msviz_details.png
   :width:  100%
   :alt: spectra and XIC details

By clicking on an PSM (gray lines) you open a view to the corresponding :ref:`annotated fragmentation spectrum <spectrum_details>` and :ref:`XIC's <xic_view>`. This allows to easily verify the quality of the match and quantify the corresponding MS1 signals. 

1. :ref:`spectrum_details`: The annotated fragmentation spectrum helps you to verfiy the quality of the match.

2. :ref:`xic_view`: 

.. _spectrum_details:

Annotated fragmentation spectrum
..................................

.. figure:: /images/msviz_spectrum.png
   :width:  100%
   :alt: spectrum details


.. _xic_view:

Extracted Ion Chromatogram (XIC)
.................................

.. figure:: /images/msviz_xic.png
   :width:  100%
   :alt: spectrum details


.. _uploads:

Uploads
-------------

Upload results
.................

.. figure:: /images/msviz_uploadResults.png
   :width:  100%
   :alt: Upload results

The types of data accepted by MsViz are either Mascot or MaxQuant results.

Select the file to upload. It will be a .zip file containing:

- Mascot: All the .MzML files used for MS1 and MS2 acquisition and .mzid file with identification results.

- MaxQuant: All the .MzML files used for MS1 and MS2 acquisition and the folder called /txt with identification results.

By clicking the button Upload your file will be loaded on MsViz.


Upload database
.................

.. figure:: /images/msviz_uploadDatabase.png
   :width:  100%
   :alt: Upload database

The database accepted by MsViz has to be a .fasta file.

By clicking the button Upload your file will be loaded on MsViz.

You can see a list of the databases you already loaded.

.. _resultBasket:

Result Basket
-------------

.. figure:: /images/msviz_resultsBasketBoth.png
   :width:  100%
   :alt: Results basket

By clicking on any of the results in the list you open a view to the selected one.

You can remove your results or you can export them into a .csv containing the protein AC, the peptide, scan number, retention time, m/z, charge, score and intensity for all your samples. 




