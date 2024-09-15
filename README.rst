================
PHI Masker Utils
================


.. image:: https://img.shields.io/pypi/v/phi_masker_utils.svg
        :target: https://pypi.python.org/pypi/phi_masker_utils

.. image:: https://img.shields.io/travis/jai-python3/phi_masker_utils.svg
        :target: https://travis-ci.com/jai-python3/phi_masker_utils

.. image:: https://readthedocs.org/projects/phi-masker-utils/badge/?version=latest
        :target: https://phi-masker-utils.readthedocs.io/en/latest/?version=latest
        :alt: Documentation Status




Collection of Python modules for masking PHI in delimited files and Excel worksheets.


* Free software: GNU General Public License v3
* Documentation: https://jai-python3.github.io/phi-masker-utils/


Usage
-----

..code-block:: python
  from phi_masker_utils import Masker

  config_file = "conf/config.yaml"
  config = yaml.safe_load(Path(config_file).read_text())

  # Tab-delimited file
  infile = "my.tsv"
  outfile = "my_masked.tsv"

  # Or comma-separated file
  infile = "my.csv"
  outfile = "my_masked.csv"

  masker = Masker(
      config=config,
      config_file=config_file,
      infile=infile,
      logfile=logfile,
      outdir=outdir,
      outfile=outfile,
      verbose=verbose,
  )

  masker.mask_phi_values()



Exported Scripts
----------------

* mask-file

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
