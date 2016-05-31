
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
3.  Result basket: look at data you added to your result basket.


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



By clicking on any of the PSM's you open a view to the corresponding spectrum and XIC's. 


