Working with Bill of Materials (BOM)
====================================

The system allows for rapid generation of manufacturing data directly from the main CAD assemblies.

Bulk BOM Export
---------------
This feature downloads the complete BOM and its associated drawings in a ZIP archive.

.. warning::
   To export a BOM, the assembly must be in the **Released** lifecycle state.

**Export Procedure:**

1. Open the tree view of the project structure.
2. Right-click the main assembly.
3. Select **Export BOM** from the context menu.
4. Wait for the background process to finish; the ZIP archive will download automatically.

.. image:: /_static/bom_export_menu.png
   :width: 600px
   :align: center
   :alt: Context menu showing the Export BOM option

Troubleshooting: Export Error
-----------------------------
If you encounter an error message regarding missing permissions during an export attempt, your assembly is likely in the *Work in Progress* state.

**Solution:** 

Check the lifecycle state of the main assembly and all its child components.
Transition them through the approval process (*In Review*) to the final *Released* state.
Then, retry the export.

User Interface Text Design (UX Microcopy)
-----------------------------------------
*This section documents internal copy changes in the UI for version 26.3.*

* **Original Error Code:** ``Err_403_state_invalid_for_export``
* **New User Text:** *This BOM cannot be exported because the CAD assembly has not yet been approved for manufacturing (Required state: Released).*
* **New Tooltip (Button Hint):** *Downloads the BOM and associated drawings in a ZIP archive.*