Developer API Reference
=======================

DataForge PDM can be integrated directly with your corporate :term:`ERP` systems using our REST API.

BOM Export
----------
This endpoint is used to programmatically download a BOM. Authentication via a Bearer token is required.

.. code-block:: http

   GET /api/v1/bom/{assembly_id}/export HTTP/1.1
   Authorization: Bearer <your_token>

**Query Parameters:**

=========== ======= ==============================================================
Parameter   Type    Description
=========== ======= ==============================================================
format      string  Desired output format. Allowed values: ``pdf``, ``xlsx``
include_dwg boolean Includes 2D drawings in the export. Default is ``false``.
=========== ======= ==============================================================

.. note::
   Calling this API on an assembly that is not in the :term:`Released` state will return a standard HTTP ``403 Forbidden`` status code.